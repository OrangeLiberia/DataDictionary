#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.buybundlesettings

# ![Tables](../../../../Images/Table32.png) [dbo].[buybundlesettings]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 61 |
| Created | 7:42:21 PM Sunday, November 1, 2020 |
| Last Modified | 7:47:59 PM Sunday, November 1, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
|  | BundleName | varchar(50) | 50 | NOT NULL |
| [![Cluster Primary Key PK_buybundlesettings: MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(50) | 50 | NOT NULL |
|  | SERVICE_TYPE | varchar(50) | 50 | NULL allowed |


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

