#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.OM_KPIS_Finance_monthly_BuyBundle_Per_Dealers

# ![Tables](../../../../Images/Table32.png) [dbo].[OM_KPIS_Finance_monthly_BuyBundle_Per_Dealers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 194344 |
| Created | 1:01:25 PM Wednesday, June 2, 2021 |
| Last Modified | 2:48:27 PM Wednesday, August 18, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK__OM_KPIS___3214EC27C9C020DD: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | CurrencyType | varchar(3) | 3 | NULL allowed |  |  |
|  | Activations | int | 4 | NULL allowed |  | _Number of Activations_ |
|  | Amount | numeric(17,2) | 9 | NULL allowed |  |  |
|  | parent_name | varchar(200) | 200 | NULL allowed |  |  |
|  | MSISDN | varchar(10) | 10 | NULL allowed |  | _MSISDN of the subscriber_ |
|  | MONTHREF | varchar(7) | 7 | NULL allowed |  |  |
|  | Bundle | varchar(200) | 200 | NULL allowed |  |  |


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

