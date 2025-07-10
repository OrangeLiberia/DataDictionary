keywords: 2G SIM, active SIM, MSISDN, last visited site, CustomerLastVisitedSite, County filter, Montserrado, Nimba, Grand Bassa, SQL Server, temp table

# FAQ: Active 2G SIM MSISDNs by Last Visited Site County

**Category:** 2G SIM Analytics  
**Last Updated:** 26 June 2025  
**Requester:** MIS BI Team  
**Responder:** David de Passos, Senior Engineer (MIS)

---

## Background  
Business analysts need to identify all active 2G SIM subscribers and determine which county they last visited on the radio network. This one-step FAQ builds a temp table of active 2G MSISDNs, then immediately joins to the last-visited-site table and filters by target counties (Montserrado, Nimba, Grand Bassa).

## Prerequisites  
- SQL Server login with read/write on the **BI** database.  
- SELECT rights on:
  - `TIMM.CRM.dbo.TIMM_Servicos_GSM`  
  - `TIMM.CRM.dbo.TIMM_Servicos`  
  - `BI.msc.CustomerLastVisitedSite`  
  - `TIMM.MEDI.dbo.DMP_SwitchCellIDs`  
- Permission to create/drop temp tables (`#2GSIM`).

## Solution Overview  
1. Switch to the **BI** database.  
2. Drop any existing `#2GSIM` temp table.  
3. Populate `#2GSIM` with distinct MSISDNs using `TipoCartaoID=1` (2G SIM) and only active services (`Status<>9`).  
4. Join `#2GSIM` to the `CustomerLastVisitedSite` table—matching the 2G MSISDN to the rightmost 8 digits of the visited‐site MSISDN.  
5. Map the returned `CellID` to `County` via the DMP SwitchCellIDs lookup.  
6. Filter results for the specified counties.

---

## SQL Script

```sql
-- ==============================================
-- Description: List active 2G SIMs by last visited site county
-- Counties    : Montserrado, Nimba, Grand Bassa
-- ==============================================

USE BI;
GO

-- 1) Clean up prior temp
DROP TABLE IF EXISTS #2GSIM;
GO

-- 2) Build temp table of active 2G MSISDNs
SELECT DISTINCT
    G.MSISDN
INTO #2GSIM
FROM [TIMM.CRM].TIMM_CRM.dbo.TIMM_Servicos_GSM AS G
INNER JOIN [TIMM.CRM].TIMM_CRM.dbo.TIMM_Servicos AS S
    ON G.MSISDN = S.MSISDN
   AND S.Status <> 9            -- only active services
WHERE G.TipoCartaoID = 1;      -- 2G SIM cards
GO

-- 3) Join to last-visited-site and map to County
SELECT
    G.MSISDN               AS Active2G_MSISDN,
    S.County               AS LastVisitedCounty
FROM #2GSIM AS G
INNER JOIN BI.msc.CustomerLastVisitedSite AS C
    ON G.MSISDN = RIGHT(C.MSISDN, 8)  -- match suffix
INNER JOIN [TIMM.MEDI].[TIMM_DMP].dbo.DMP_SwitchCellIDs AS S
    ON C.CellID = S.ID
WHERE S.County IN ('Montserrado', 'Nimba', 'Grand Bassa')
ORDER BY G.MSISDN;
GO
