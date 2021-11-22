#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.customerUsage

# ![Tables](../../../../Images/Table32.png) [dbo].[customerUsage]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 4 |
| Created | 6:40:20 PM Tuesday, March 30, 2021 |
| Last Modified | 6:40:20 PM Tuesday, March 30, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| Partner | varchar(256) | 256 | NULL allowed |  |
| CustomerTopUpValue | decimal(38,6) | 17 | NULL allowed |  |
| CustomerTopUpVolume | int | 4 | NULL allowed |  |


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

