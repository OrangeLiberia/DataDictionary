#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.TDR_Dup

# ![Tables](../../../../Images/Table32.png) [dbo].[TDR_Dup]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Compression | ROW |
| Row Count (~) | 265540 |
| Created | 3:49:51 PM Thursday, November 19, 2020 |
| Last Modified | 3:17:57 AM Friday, November 27, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| FileID | bigint | 8 | NULL allowed |  |
| CDRID | int | 4 | NULL allowed |  |
| RefFileDate | date | 3 | NULL allowed |  |
| TransactionKey | bigint | 8 | NULL allowed |  |
| SUBS_NUMBER | varchar(32) | 32 | NULL allowed |  |
| ChargeableAmount | decimal(28,6) | 13 | NULL allowed |  |
| TIME | datetime | 8 | NULL allowed |  |
| CARD_SERIAL_NUMBER | varchar(4000) | 4000 | NULL allowed |  |
| TDR_ENDING_BALANCE | decimal(28,6) | 13 | NULL allowed |  |
| WALLET_TYPE | int | 4 | NULL allowed | _IN Wallet type_ |
| CLEAR_CAUSE | decimal(28,0) | 13 | NULL allowed |  |
| COMMENTS | varchar(4000) | 4000 | NULL allowed |  |
| CHARGEABLE_WALLET_TYPE | int | 4 | NULL allowed |  |
| SPARE1 | varchar(4000) | 4000 | NULL allowed |  |
| SPARE2 | varchar(4000) | 4000 | NULL allowed |  |
| SPARE3 | varchar(4000) | 4000 | NULL allowed |  |
| SPARE4 | varchar(4000) | 4000 | NULL allowed |  |
| SPARE5 | varchar(4000) | 4000 | NULL allowed |  |
| SPARE6 | varchar(4000) | 4000 | NULL allowed |  |
| SPARE7 | varchar(4000) | 4000 | NULL allowed |  |


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

