#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.OMKPIS_Cohort

# ![Tables](../../../../Images/Table32.png) [dbo].[OMKPIS_Cohort]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 2235 |
| Created | 11:13:44 PM Tuesday, May 25, 2021 |
| Last Modified | 11:13:44 PM Tuesday, May 25, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__OMKPIS_C__3214EC27612541E4: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | Refdate | date | 3 | NULL allowed |  |
|  | Label | varchar(200) | 200 | NULL allowed |  |
|  | Total | int | 4 | NULL allowed |  |
|  | CohortMonth | varchar(7) | 7 | NULL allowed |  |
|  | ActivityMonth | varchar(7) | 7 | NULL allowed |  |


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

* [dbo].[OMKPIS_bactchsps]
* [dbo].[spc_OMKPIS_Batchsps]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

