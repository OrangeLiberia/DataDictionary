#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.usdtemplate

# ![Tables](../../../../Images/Table32.png) [dbo].[usdtemplate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 33311 |
| Created | 1:43:26 PM Friday, May 7, 2021 |
| Last Modified | 1:43:26 PM Friday, May 7, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| MSISDN* | varchar(15) | 15 | NOT NULL |
| User Type* (Subscriber/Channel User) | varchar(10) | 10 | NOT NULL |
| MFS Id* | varchar(3) | 3 | NOT NULL |
| Wallet Id* | int | 4 | NOT NULL |
| Grade Code | varchar(7) | 7 | NOT NULL |
| Transfer Profile ID | varchar(20) | 20 | NOT NULL |
| Web Group Role Code | varchar(1) | 1 | NOT NULL |
| Mobile Group Role Code | varchar(9) | 9 | NOT NULL |


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

