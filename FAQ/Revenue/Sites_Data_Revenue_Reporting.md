# FAQ: Sites Data & Revenue Reporting

## Keywords  
- BI server  
- TIMM_INV.TIMM_DMP  
- DMP_SwitchCellIDs  
- Global_SiteID  
- County  
- CellID  
- #Sites, #Sites2  
- SubsCallsPerCellDeviceMonthly  
- SubsTransactionsPerCellMonthly  
- fwk.DimDate  
- TransactionKeys  
- WalletID  
- Minutes, Amount, NSubs  
- SSIS / SQL Agent Job  
- Parameterization  

---

## Overview  
**Q: What’s the purpose of this report?**  
A: To deliver daily traffic (voice & data), revenue (GSM voice, GSM data, OM), and subscriber counts by site—helping you monitor ERA-site performance at a glance.

---

## Data Sources & Environment  

**Q: Which server and database houses the raw site data?**  
A:  
- **Server:** Your BI server  
- **Database:** `TIMM.INV.TIMM_DMP`  

**Q: What tables feed into this report?**  
A:  
1. **`DMP_SwitchCellIDs`** – maps each CellID to a `Global_SiteID` and `County`.  
2. **`SubsCallsPerCellDeviceMonthly`** – call records (minutes, amounts) per MSISDN and CellID.  
3. **`SubsTransactionsPerCellMonthly`** – data & transaction records per MSISDN and CellID.  
4. **`fwk.DimDate`** – date dimension to filter by reporting period.  
5. **`[in].TransactionKeys`** – filters only billable transactions.

---

## Generating the Site Lists  

**Q: How do I build the list of all “Sites” per `Global_SiteID`?**  
A: Two temp tables are used:

```sql
-- 1) Raw mapping of CellID → Global_SiteID & County  
SELECT *
INTO #Sites
FROM [TIMM.INV].[TIMM_DMP].[dbo].[DMP_SwitchCellIDs];

-- 2) Concatenate CellIDs per Global_SiteID for easy lookup  
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
GROUP BY CAT.Global_SiteID, CAT.County
ORDER BY CAT.Global_SiteID;
