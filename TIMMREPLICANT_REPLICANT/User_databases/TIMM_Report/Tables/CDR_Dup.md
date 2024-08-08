#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.CDR_Dup

# ![Tables](../../../../Images/Table32.png) [dbo].[CDR_Dup]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 854 |
| Created | 5:23:52 PM Thursday, November 19, 2020 |
| Last Modified | 5:23:52 PM Thursday, November 19, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| FileID | bigint | 8 | NULL allowed |  |
| CDRID | int | 4 | NULL allowed |  |
| RefFileDate | date | 3 | NULL allowed |  |
| CLEAR_CAUSE | decimal(28,0) | 13 | NULL allowed |  |
| SUBS_NUMBER | varchar(32) | 32 | NULL allowed |  |
| PRODUCT_TYPE | decimal(28,0) | 13 | NULL allowed |  |
| EVENT_PARAMETER1 | varchar(4000) | 4000 | NULL allowed |  |
| SL_SEIZE_TIME | datetime | 8 | NULL allowed |  |
| ORIGINATE_TIME | datetime | 8 | NULL allowed |  |
| ANSWER_TIME | datetime | 8 | NULL allowed | _Inicial time of the call_ |
| DISCONNECT_TIME | datetime | 8 | NULL allowed | _End time of the call_ |
| TRANSACTION_TIME | datetime | 8 | NULL allowed |  |
| CHARGEABLE_DURATION | decimal(28,0) | 13 | NULL allowed | _Duration of the call rounded_ |
| WALLET_TYPE_ID | int | 4 | NULL allowed |  |
| ENDING_BALANCE | decimal(28,6) | 13 | NULL allowed |  |
| AMOUNT_CHARGED | decimal(28,6) | 13 | NULL allowed | _Amount charged_ |
| PRODUCT_ID | bigint | 8 | NULL allowed |  |
| COMMENTS | varchar(4000) | 4000 | NULL allowed |  |
| COUNTER_ID | bigint | 8 | NULL allowed |  |
| BUNDLE_ID | bigint | 8 | NULL allowed |  |


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

