keywords: Sites Data, daily traffic, voice, data, revenue, GSM, OM, users, ERA Sites, SQL script, DMP_SwitchCellIDs  

# FAQ: Retrieve Daily Traffic, Revenue & Users by Site  

**Request:**  
“Please is there a table or way that I can get the daily traffic (Voice & Data), revenue (GSM (voice, data) & OM) and users (GSM, OM) by Sites. We need it to know the performance of the ERA Sites.”  
— Henry N Bainda, 18 June 2025  

**Answer:**  
Use the MIS BI database on SQL Server to pull per-site metrics in three steps:  

1. Build a temp table of all CellID→Site mappings.  
2. Collapse CellIDs into a comma-delimited list per `Global_SiteID`.  
3. Join calls + transactions, aggregate minutes, amounts and distinct subscribers.  

```sql
-- 1) Load raw cell-to-site mapping
SELECT *
INTO #Sites
FROM [TIMM.INV].[TIMM_DMP].[dbo].[DMP_SwitchCellIDs];

-- 2) Aggregate CellIDs per Global_SiteID
SELECT
  CAT.Global_SiteID,
  CAT.County,
  STUFF((
    SELECT ',' + CONVERT(VARCHAR(10), SUB.ID)
    FROM [TIMM.INV].[TIMM_DMP].[dbo].[DMP_SwitchCellIDs] SUB
    WHERE SUB.Global_SiteID = CAT.Global_SiteID
    FOR XML PATH(''), TYPE
  ).value('.', 'NVARCHAR(MAX)'), 1, 1, '') AS Sites
INTO #Sites2
FROM [TIMM.INV].[TIMM_DMP].[dbo].[DMP_SwitchCellIDs] CAT
GROUP BY CAT.Global_SiteID, CAT.County;

-- 3) Combine traffic, revenue & user counts by site/month
SELECT
  RSM.[Month],
  SL.County,
  SL.Global_SiteID,
  SL.Sites,
  RSM.[Minutes],
  RSM.Amount,
  RSM.NSubs
FROM (
  -- Aggregate per site-month
  SELECT
    RCM.[Month],
    CL.County,
    CL.Global_SiteID,
    SUM(RCM.[Minutes])         AS [Minutes],
    SUM(RCM.Amount)            AS Amount,
    COUNT(DISTINCT RCM.MSISDN) AS NSubs
  FROM (
    -- Outgoing voice calls (minutes)
    SELECT
      DD.DtYMD      AS [Month],
      CMI.MSISDN,
      CMI.CellID,
      (CMI.MOFreeDurSec + CMI.MOChargedDurSec)/60.0 AS [Minutes],
      CASE WHEN CMI.WalletID IN (2,3) THEN CMI.Amount ELSE 0 END AS Amount
    FROM [in].[SubsCallsPerCellDeviceMonthly] CMI
    INNER JOIN fwk.DimDate DD
      ON DD.ID = CMI.IDDimDate
      AND DD.IDPeriodYM = 202404
    WHERE CMI.CellID >= 1000

    UNION ALL

    -- Data & other transactions (negative amounts)
    SELECT
      DD.DtYMD      AS [Month],
      TMI.MSISDN,
      TMI.CellID,
      0             AS [Minutes],
      -1 * TMI.Amount AS Amount
    FROM [in].[SubsTransactionsPerCellMonthly] TMI
    INNER JOIN fwk.DimDate DD
      ON DD.ID = TMI.IDDimDate
      AND DD.IDPeriodYM = 202404
    INNER JOIN [in].TransactionKeys TR
      ON TR.ID = TMI.TransactionKey
      AND (TR.Fee = 1 OR TR.FeeOM = 1)
      AND TR.Type IS NOT NULL
      AND TR.IDOrigDest IS NOT NULL
    WHERE TMI.CellID >= 1000
      AND TMI.WalletID IN (2,3,90,91)
  ) RCM
  INNER JOIN #Sites CL
    ON CL.ID = RCM.CellID
  GROUP BY RCM.[Month], CL.County, CL.Global_SiteID
) RSM
INNER JOIN #Sites2 SL
  ON SL.Global_SiteID = RSM.Global_SiteID;
