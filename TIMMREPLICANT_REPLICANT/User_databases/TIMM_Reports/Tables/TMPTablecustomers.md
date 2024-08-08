#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.TMPTablecustomers

# ![Tables](../../../../Images/Table32.png) [dbo].[TMPTablecustomers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 1194431996 |
| Created | 4:54:08 PM Thursday, August 13, 2020 |
| Last Modified | 4:13:23 PM Sunday, August 16, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| refdate | date | 3 | NULL allowed |
| refhour | int | 4 | NULL allowed |
| servedmsisdn | varchar(32) | 32 | NULL allowed |
| dataVolumeGPRSUplink | bigint | 8 | NULL allowed |
| dataVolumeGPRSDownlink | bigint | 8 | NULL allowed |
| duration | int | 4 | NULL allowed |
| CellID | varchar(225) | 225 | NULL allowed |
| county | varchar(225) | 225 | NULL allowed |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | SELECT | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | SELECT | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | SELECT | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | SELECT | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | SELECT | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

