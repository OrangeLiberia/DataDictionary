#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_ShortCodesCDRsConfigNumbers

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_ShortCodesCDRsConfigNumbers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 451 |
| Created | 6:34:26 PM Monday, May 11, 2020 |
| Last Modified | 7:03:49 PM Thursday, July 22, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK__tbc_Shor__CCA4BF6612B22581: Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | ShortCode | varchar(12) | 12 | NOT NULL |  |  |
| [![Cluster Primary Key PK__tbc_Shor__CCA4BF6612B22581: Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(12) | 12 | NOT NULL |  |  |
|  | Name | varchar(100) | 100 | NULL allowed |  | _Name_ |
|  | Price | decimal(18,6) | 9 | NULL allowed |  |  |
|  | Status | int | 4 | NULL allowed |  |  |
| [![Cluster Primary Key PK__tbc_Shor__CCA4BF6612B22581: Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | OrigDest | varchar(20) | 20 | NOT NULL | ('All') | _Origin or Destination type_ |


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

## <a name="#usedby"></a>Used By

* [dbo].[spc_CodeName]
* [dbo].[spc_FreeIncomingMinutes]
* [dbo].[spc_FreeIncomingMinutesDaily]
* [dbo].[spc_FreeIncomingMinutesMonthly]
* [dbo].[spc_ShortcodesCDR]
* [dbo].[spc_ShortcodesCDROrigin]
* [dbo].[spc_ShortCodesCDRs]
* [dbo].[spc_ShortCodesCDRs_aux]
* [dbo].[spc_ShortcodesGroupedCDRsDaily]
* [dbo].[spc_ShortcodesGroupedCDRsMonth]
* [dbo].[spc_ShortcodesGroupedCDRsMonthly]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

