keywords: Sites Data, daily traffic, voice, data, revenue, GSM, OM, users, ERA Sites, SQL Server, temp tables, aggregation

# FAQ: Retrieve Daily Traffic, Revenue & User Counts by Site

**Category:** Site Performance  
**Last Updated:** 26 June 2025  

---

## Background  
Field teams and management need a daily breakdown of voice minutes, data-related transactions (revenue and subscriber counts) per cell site, so they can track performance of ERA Sites across counties.

## Prerequisites  
- SQL Server access to the **TIMM.INV** instance.  
- Read permissions on:
  - `TIMM_DMP.dbo.DMP_SwitchCellIDs`
  - `in.SubsCallsPerCellDeviceMonthly`
  - `in.SubsTransactionsPerCellMonthly`
  - `fwk.DimDate`
  - `in.TransactionKeys`  
- Ability to create temp tables in tempdb.

## Solution Overview  
1. **Map each CellID to a Global_SiteID** using `DMP_SwitchCellIDs`.  
2. **Flatten** each site's multiple CellIDs into a comma-separated list.  
3. **Union** call and transaction data to get minutes and revenue.  
4. **Aggregate** by date + site, and count distinct subscribers.  
5. **Join** back to the CellID list for a final, human-readable report.

---

## SQL Script

```sql
-- ==============================================
-- Description: Daily voice/data metrics per site
-- Dependencies: see Prerequisites above
-- Parameter : @PeriodYM  INT = YYYYMM filter (e.g., 202406)
-- ==============================================

DECLARE @PeriodYM INT = 202406;  -- adjust as needed

-- 1) Raw mapping: CellID → Global_SiteID + County
SELECT
  ID            AS CellID,     
  Global_SiteID,
  County
INTO #Sites
FROM [TIMM.INV].[TIMM_DMP].dbo.DMP_SwitchCellIDs;

-- 2) Build comma-delimited CellID list per site
SELECT
  CAT.Global_SiteID,
  CAT.County,
  STUFF((
    SELECT ',' + CONVERT(VARCHAR(10), SUB.ID)
    FROM [TIMM.INV].[TIMM_DMP].dbo.DMP_SwitchCellIDs AS SUB
    WHERE SUB.Global_SiteID = CAT.Global_SiteID
    FOR XML PATH(''), TYPE
  ).value('.', 'NVARCHAR(MAX)'), 1, 1, '') AS CellList
INTO #Sites2
FROM [TIMM.INV].[TIMM_DMP].dbo.DMP_SwitchCellIDs AS CAT
GROUP BY CAT.Global_SiteID, CAT.County;

-- 3) Combine metrics from calls + transactions
WITH RawMetrics AS (
  -- 3a) Outgoing voice calls → minutes + wallet-based revenue
  SELECT
    DD.DtYMD         AS [Date],
    CMI.MSISDN,
    CMI.CellID,
    (CMI.MOFreeDurSec + CMI.MOChargedDurSec)/60.0 AS Minutes,
    CASE WHEN CMI.WalletID IN (2,3) THEN CMI.Amount ELSE 0 END AS Amount
  FROM [in].SubsCallsPerCellDeviceMonthly AS CMI
  JOIN fwk.DimDate AS DD
    ON DD.ID = CMI.IDDimDate
   AND DD.IDPeriodYM = @PeriodYM
  WHERE CMI.CellID >= 1000

  UNION ALL

  -- 3b) Data & non-voice transactions → negative revenue for deductions
  SELECT
    DD.DtYMD          AS [Date],
    TMI.MSISDN,
    TMI.CellID,
    0                 AS Minutes,
    -1 * TMI.Amount   AS Amount
  FROM [in].SubsTransactionsPerCellMonthly AS TMI
  JOIN fwk.DimDate AS DD
    ON DD.ID = TMI.IDDimDate
   AND DD.IDPeriodYM = @PeriodYM
  JOIN [in].TransactionKeys AS TR
    ON TR.ID = TMI.TransactionKey
   AND (TR.Fee = 1 OR TR.FeeOM = 1)
   AND TR.Type IS NOT NULL
   AND TR.IDOrigDest IS NOT NULL
  WHERE TMI.WalletID IN (2,3,90,91)
),

SiteMetrics AS (
  -- 3c) Aggregate by date + site
  SELECT
    RM.[Date],
    S.County,
    S.Global_SiteID,
    SUM(RM.Minutes)           AS TotalMinutes,
    SUM(RM.Amount)            AS TotalRevenue,
    COUNT(DISTINCT RM.MSISDN) AS SubscriberCount
  FROM RawMetrics AS RM
  JOIN #Sites AS S
    ON S.CellID = RM.CellID
  GROUP BY RM.[Date], S.County, S.Global_SiteID
)

-- 4) Final output: join site metrics with cell lists
SELECT
  SM.[Date],
  SM.County,
  SM.Global_SiteID,
  S2.CellList,
  SM.TotalMinutes   AS VoiceMinutes,
  SM.TotalRevenue   AS Revenue,
  SM.SubscriberCount
FROM SiteMetrics AS SM
JOIN #Sites2 AS S2
  ON S2.Global_SiteID = SM.Global_SiteID
ORDER BY SM.[Date], SM.County, SM.Global_SiteID;
