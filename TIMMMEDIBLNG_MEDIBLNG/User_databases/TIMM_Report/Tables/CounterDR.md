#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.CounterDR

# ![Tables](../../../../Images/Table32.png) [dbo].[CounterDR]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 0 |
| Created | 4:22:30 PM Monday, October 28, 2019 |
| Last Modified | 4:22:30 PM Monday, October 28, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| FileID | bigint | 8 | NULL allowed |  |
| CDRID | int | 4 | NULL allowed |  |
| RefFileDate | date | 3 | NULL allowed |  |
| COUNTER_ID | bigint | 8 | NULL allowed |  |
| SUBS_NUMBER | varchar(32) | 32 | NULL allowed |  |
| COUNTER_VALUE | decimal(38,0) | 17 | NULL allowed |  |
| EXPIRATION_DATE | datetime | 8 | NULL allowed | _Date and time of the Bundle deactivation_ |
| COMMENTS | varchar(4000) | 4000 | NULL allowed |  |
| EVENTTIME | datetime | 8 | NULL allowed |  |
| WALLET_TYPE | int | 4 | NULL allowed | _IN Wallet type_ |
| CHARGEABLE_WALLET_TYPE_ID | int | 4 | NULL allowed |  |


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

