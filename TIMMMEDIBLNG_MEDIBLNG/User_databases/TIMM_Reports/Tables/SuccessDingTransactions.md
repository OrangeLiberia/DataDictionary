#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.SuccessDingTransactions

# ![Tables](../../../../Images/Table32.png) [dbo].[SuccessDingTransactions]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 209 |
| Created | 2:22:35 PM Friday, April 16, 2021 |
| Last Modified | 2:22:35 PM Friday, April 16, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| transaction_date | nvarchar(50) | 100 | NOT NULL |
| prod_name | nvarchar(50) | 100 | NOT NULL |
| oper_name | nvarchar(50) | 100 | NOT NULL |
| MSISDN | varchar(50) | 50 | NOT NULL |
| subscriber_number | varchar(50) | 50 | NOT NULL |
| receive_amount | varchar(50) | 50 | NOT NULL |
| ezetop_transaction_ID | varchar(50) | 50 | NOT NULL |


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

