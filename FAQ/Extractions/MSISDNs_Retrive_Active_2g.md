keywords: 2G SIM, last visited site, CustomerLastVisitedSite, County, Montserrado, Nimba, Grand Bassa, #2GSIM, DMP_SwitchCellIDs

# FAQ: Retrieve Active 2G SIM MSISDNs by Last Visited Site County

**Category:** Site-Level Usage Analysis  
**Last Updated:** 26 June 2025  
**Prerequisite FAQ:** Extract Active 2G SIM MSISDNs into `#2GSIM`  
**Requester:** MIS BI Team  
**Responder:** David de Passos, Senior Engineer (MIS)

---

## Background  
After isolating active 2G SIMs in the `#2GSIM` temp table, analysts often need to know where those subscribers last connected on the radio network. This query ties each MSISDN to its last visited cell site and filters by specific counties (Montserrado, Nimba, Grand Bassa) for targeted regional reporting.

## Prerequisites  
- A populated temp table `#2GSIM` (see “Extract Active 2G SIM MSISDNs” FAQ).  
- Access to the **BI** database and schemas:  
  - `msc.CustomerLastVisitedSite` (stores last‐seen CellID per MSISDN)  
  - `TIMM.MEDI.dbo.DMP_SwitchCellIDs` (maps CellID → County)  
- Permissions to SELECT from those tables and to use temp tables.

## Solution Overview  
1. Switch context to the **BI** database.  
2. Join `#2GSIM` to `msc.CustomerLastVisitedSite` by matching the 8-digit MSISDN suffix.  
3. Map the returned `CellID` to a `County` via the DMP switch-cell table.  
4. Filter for the counties of interest.  

---

## SQL Script

```sql
-- ==============================================
-- Description: List active 2G MSISDNs by last visited site county
-- Dependencies: #2GSIM must already exist
-- Filters      : Montserrado, Nimba, Grand Bassa
-- ==============================================

USE BI;
GO

SELECT
  G.MSISDN,
  S.County
FROM
  #2GSIM AS G
  -- Match active 2G numbers to their last visited site record
  INNER JOIN BI.msc.CustomerLastVisitedSite AS C
    ON G.MSISDN = RIGHT(C.MSISDN, 8)
  -- Resolve CellID to human‐readable County
  INNER JOIN TIMM.MEDI.dbo.DMP_SwitchCellIDs AS S
    ON C.CellID = S.ID
WHERE
  S.County IN ('Montserrado', 'Nimba', 'Grand Bassa');
GO
