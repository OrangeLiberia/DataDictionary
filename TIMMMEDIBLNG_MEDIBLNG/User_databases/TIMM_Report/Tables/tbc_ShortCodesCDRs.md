#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_ShortCodesCDRs

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_ShortCodesCDRs]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 12558 |
| Created | 5:33:56 PM Monday, May 11, 2020 |
| Last Modified | 1:43:31 PM Monday, January 18, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK__tbc_Shor__069642F41B7A6360: DayReference\Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | DayReference | smalldatetime | 4 | NOT NULL |  | _Day_ |
| [![Cluster Primary Key PK__tbc_Shor__069642F41B7A6360: DayReference\Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(12) | 12 | NOT NULL |  |  |
| [![Cluster Primary Key PK__tbc_Shor__069642F41B7A6360: DayReference\Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | ShortCode | varchar(9) | 9 | NOT NULL |  |  |
|  | Seconds | bigint | 8 | NULL allowed |  | _Number of Seconds of the call_ |
|  | NumberOfCalls | int | 4 | NULL allowed |  |  |
|  | AmountIN | decimal(18,6) | 9 | NULL allowed |  | _Amount charged in the IN_ |
|  | AmountCalculated | decimal(18,6) | 9 | NULL allowed |  | _Amount calculated by configuration_ |
| [![Cluster Primary Key PK__tbc_Shor__069642F41B7A6360: DayReference\Type\ShortCode\OrigDest](../../../../Images/pkcluster.png)](#indexes) | OrigDest | varchar(20) | 20 | NOT NULL | ('All') | _Origin or Destination type_ |


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

* [dbo].[spc_FreeIncomingMinutes]
* [dbo].[spc_FreeIncomingMinutesDaily]
* [dbo].[spc_FreeIncomingMinutesMonthly]
* [dbo].[spc_ShortCodesCDRs]
* [dbo].[spc_ShortCodesCDRs_aux]
* [dbo].[spc_ShortcodesGroupedCDRsDaily]
* [dbo].[spc_ShortcodesGroupedCDRsMonth]
* [dbo].[spc_ShortcodesGroupedCDRsMonthly]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

