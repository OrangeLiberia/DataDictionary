keywords: 2G SIM, MSISDN, TIMM_Servicos_GSM, TipoCartaoID, active services, CRM data, temp table  

# FAQ: Extract Active 2G SIM MSISDNs into a Temp Table

**Category:** CRM Data Extraction  
**Last Updated:** 26 June 2025  
**Requester:** MIS BI Team  
**Responder:** David de Passos, Senior Engineer (MIS)

---

## Background  
Business analysts need a quick way to isolate all MSISDNs (mobile numbers) provisioned on 2G SIM cards that remain in service (i.e., not deactivated). We’ll populate a transient temp table `#2GSIM` for downstream processing (joins, filters, reporting).

## Prerequisites  
- SQL Server login with read/write on the **BI** database.  
- SELECT on:
  - `TIMM.CRM.dbo.TIMM_Servicos_GSM`  
  - `TIMM.CRM.dbo.TIMM_Servicos`  
- Permissions to create and drop temp tables.

## Solution Overview  
1. Switch context to the **BI** database.  
2. Drop any pre-existing `#2GSIM` temp table.  
3. Query the GSM-services table, filter for 2G SIMs (`TipoCartaoID = 1`).  
4. Exclude records whose status in the master services table is “9” (deactivated).  
5. Select distinct MSISDNs into `#2GSIM`.

---

## SQL Script

```sql
-- ==============================================
-- Description: Build temp table of active 2G SIM MSISDNs
-- Usage      : downstream joins or exports
-- ==============================================

USE BI;
GO

-- Remove prior temp table if present
DROP TABLE IF EXISTS #2GSIM;
GO

-- Populate #2GSIM with unique MSISDNs on 2G SIM (TipoCartaoID=1)
-- and only those still active (Status <> 9)
SELECT DISTINCT
    G.MSISDN
INTO #2GSIM
FROM [TIMM.CRM].TIMM_CRM.dbo.TIMM_Servicos_GSM AS G
INNER JOIN [TIMM.CRM].TIMM_CRM.dbo.TIMM_Servicos AS S
    ON G.MSISDN = S.MSISDN
   AND S.Status <> 9
WHERE G.TipoCartaoID = 1;
GO

-- Verify row count
SELECT COUNT(*) AS Active2GCount FROM #2GSIM;
GO
