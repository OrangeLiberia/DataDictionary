#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.bblparent

# ![Tables](../../../../Images/Table32.png) [dbo].[bblparent]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 129057 |
| Created | 5:38:21 PM Monday, May 3, 2021 |
| Last Modified | 5:38:21 PM Monday, May 3, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| currencytype | varchar(16) | 16 | NOT NULL |
| Activations | int | 4 | NULL allowed |
| Amount | numeric(38,2) | 17 | NULL allowed |
| Parent_Name | varchar(200) | 200 | NULL allowed |
| SENDER_MSISDN | varchar(15) | 15 | NOT NULL |
| MonthRef | varchar(7) | 7 | NULL allowed |
| Bundle | varchar(128) | 128 | NULL allowed |


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

