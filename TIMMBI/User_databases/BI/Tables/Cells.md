#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.Cells

# ![Tables](../../../../Images/Table32.png) [msc].[Cells]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Cells: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | Name | varchar(50) | 50 | NOT NULL |
|  | LAC | int | 4 | NULL allowed |
|  | Technology | varchar(20) | 20 | NULL allowed |
|  | Generation | varchar(5) | 5 | NULL allowed |
| [![Foreign Keys FK_Cells_Site: [msc].[Sites].IDSite](../../../../Images/fk.png)](#foreignkeys) | IDSite | int | 4 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Cells: ID](../../../../Images/pkcluster.png)](#indexes) | PK_Cells | ID | YES | MSC |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Cells_Site | IDSite->[[msc].[Sites].[ID]](Sites.md) |


---

## <a name="#uses"></a>Uses

* [[msc].[Sites]](Sites.md)
* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[CellsSitesLocation]](../Views/CellsSitesLocation.md)
* [[msc].[CellsSitesLocation_Basic]](../Views/CellsSitesLocation_Basic.md)
* [[TIMM_Reports].[dbo].[Sanza_Campaign]](../../TIMM_Reports/Programmability/Stored_Procedures/Sanza_Campaign.md)
* [[External].[dbo].[spc_SpeciallyForGregDailyMinutesPerSite]](../../External/Programmability/Stored_Procedures/spc_SpeciallyForGregDailyMinutesPerSite.md)
* [[msc].[spc_LoadCellReleaseCauses]](../Programmability/Stored_Procedures/spc_LoadCellReleaseCauses.md)
* [[msc].[spc_UpdateListTables]](../Programmability/Stored_Procedures/spc_UpdateListTables.md)
* [[msc].[spt_GetCellReleaseCausesDaily]](../Programmability/Stored_Procedures/spt_GetCellReleaseCausesDaily.md)
* [[msc].[spt_GetCellTrafficDaily]](../Programmability/Stored_Procedures/spt_GetCellTrafficDaily.md)
* [[msc].[spt_GetCellTrafficMonthly]](../Programmability/Stored_Procedures/spt_GetCellTrafficMonthly.md)
* [[msc].[fnc_GetSiteHostedCells]](../Programmability/Functions/Scalar-valued_Functions/fnc_GetSiteHostedCells.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

