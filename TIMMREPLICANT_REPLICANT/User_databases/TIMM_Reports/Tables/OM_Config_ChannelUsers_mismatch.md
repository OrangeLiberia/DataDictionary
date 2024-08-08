#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.OM_Config_ChannelUsers_mismatch

# ![Tables](../../../../Images/Table32.png) [dbo].[OM_Config_ChannelUsers_mismatch]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 52 |
| Created | 3:39:48 PM Tuesday, May 25, 2021 |
| Last Modified | 3:39:48 PM Tuesday, May 25, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__OM_Confi__3214EC27811307E0: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | DESIGNATION | varchar(200) | 200 | NULL allowed |  |
|  | DESCRIPTION | varchar(200) | 200 | NULL allowed |  |


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

* [TIMM_Report].[dbo].[spc_OMKPIS_Distribution_Overview]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

