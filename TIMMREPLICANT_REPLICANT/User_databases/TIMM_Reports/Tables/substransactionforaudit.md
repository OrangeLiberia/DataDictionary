#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.substransactionforaudit

# ![Tables](../../../../Images/Table32.png) [dbo].[substransactionforaudit]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 184379 |
| Created | 12:58:34 PM Friday, January 15, 2021 |
| Last Modified | 12:58:34 PM Friday, January 15, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__substran__3214EC2793FCF65E: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | USERNAME | varchar(100) | 100 | NULL allowed |  |
|  | MSISDN | varchar(100) | 100 | NULL allowed |  |
|  | OTHER_MSISDN | varchar(100) | 100 | NULL allowed |  |
|  | TRANSACTION_AMOUNT | numeric(32,2) | 17 | NULL allowed |  |
|  | SERVICE_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | RefDate | date | 3 | NULL allowed |  |
|  | TRANSFER_DATETIME | datetime | 8 | NULL allowed |  |
|  | CurrencyType | varchar(100) | 100 | NULL allowed |  |
|  | RECEIVER_DOMAIN_CODE | varchar(100) | 100 | NULL allowed |  |
|  | USERDOMAIN | varchar(100) | 100 | NULL allowed |  |
|  | MSISDN_Pre_Balance | varchar(100) | 100 | NULL allowed |  |
|  | MSISDN_POST_Balance | varchar(100) | 100 | NULL allowed |  |
|  | TRANSFER_SUBTYPE | varchar(100) | 100 | NULL allowed |  |
|  | MSISDNWALLET | varchar(100) | 100 | NULL allowed |  |
|  | OTHERWALLET | varchar(100) | 100 | NULL allowed |  |


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

