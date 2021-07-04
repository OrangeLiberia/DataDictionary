#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.Sites

# ![Tables](../../../../Images/Table32.png) [msc].[Sites]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Sites: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int |  | 4 | NOT NULL | 1 - 1 |
|  | Name | varchar(100) |  | 100 | NULL allowed |  |
|  | County | varchar(100) |  | 100 | NULL allowed |  |
|  | Location | varchar(50) |  | 50 | NULL allowed |  |
|  | UnifiedCellID | int |  | 4 | NULL allowed |  |
|  | Latitude | numeric(10,6) |  | 9 | NOT NULL |  |
|  | Longitude | numeric(10,6) |  | 9 | NOT NULL |  |
|  | SpatialData | geography |  | max | NOT NULL |  |
|  | CellsHosted | varchar(500) | YES | 500 | NULL allowed |  |
|  | UnifiedSiteName | nvarchar(4000) | YES | 8000 | NULL allowed |  |
|  | UnifiedSiteNameLong | nvarchar(4000) | YES | 8000 | NULL allowed |  |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| CellsHosted | ([msc].[fnc_GetSiteHostedCells]([ID])) |
| UnifiedSiteName | (replace(replace('[$CellID] [$SiteName]','[$CellID]',quotename(CONVERT([varchar],[UnifiedCellID],(0)))),'[$SiteName]',[Name])) |
| UnifiedSiteNameLong | (replace(replace(replace(replace('[$CellID] [$SiteName] ([$LAT], [$LONG])','[$CellID]',quotename(CONVERT([varchar],[UnifiedCellID],(0)))),'[$SiteName]',[Name]),'[$LAT]',CONVERT([varchar],CONVERT([decimal](10,4),[Longitude],(0)),(0))),'[$LONG]',CONVERT([varchar],CONVERT([decimal](10,4),[Latitude],(0)),(0)))) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Sites: ID](../../../../Images/pkcluster.png)](#indexes) | PK_Sites | ID | YES | MSC |


---

## <a name="#uses"></a>Uses

* [[msc].[fnc_GetSiteHostedCells]](../Programmability/Functions/Scalar-valued_Functions/fnc_GetSiteHostedCells.md)
* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[Cells]](Cells.md)
* [[msc].[CellsSitesLocation]](../Views/CellsSitesLocation.md)
* [[msc].[CellsSitesLocation_Basic]](../Views/CellsSitesLocation_Basic.md)
* [[TIMM_Reports].[dbo].[rpt_RevenuePerSite]](../../TIMM_Reports/Programmability/Stored_Procedures/rpt_RevenuePerSite.md)
* [[in].[spc_GetConsumptionPerSite]](../Programmability/Stored_Procedures/spc_GetConsumptionPerSite.md)
* [[in].[spc_GetRevenueTotalPerSite]](../Programmability/Stored_Procedures/spc_GetRevenueTotalPerSite.md)
* [[in].[spc_GetTransactionsTotalPerSite]](../Programmability/Stored_Procedures/spc_GetTransactionsTotalPerSite.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

