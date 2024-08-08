#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.orangemoneytotalbasegrowth

# ![Tables](../../../../Images/Table32.png) [dbo].[orangemoneytotalbasegrowth]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 21 |
| Created | 6:00:05 PM Wednesday, September 2, 2020 |
| Last Modified | 6:00:05 PM Wednesday, September 2, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__orangemo__3214EC27CB5FC040: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Currentmonth | varchar(10) | 10 | NULL allowed |  |
|  | TotalBaseMOM | int | 4 | NULL allowed |  |
|  | TotalBaseValidMOM | int | 4 | NULL allowed |  |
|  | TotalBaseInvalidMOM | int | 4 | NULL allowed |  |
|  | TotalBaseUncheckedMOM | int | 4 | NULL allowed |  |
|  | ComplianceRateMOM | numeric(10,5) | 9 | NULL allowed |  |


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

