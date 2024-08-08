#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.CDR

# ![Tables](../../../../Images/Table32.png) [dbo].[CDR]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Compression | ROW |
| Row Count (~) | 50735010 |
| Created | 2:04:01 PM Monday, October 28, 2019 |
| Last Modified | 4:37:32 PM Wednesday, December 2, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CDR: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_CDR: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |  |
|  | RefFileDate | date | 3 | NULL allowed |  |
|  | CLEAR_CAUSE | decimal(28,0) | 13 | NULL allowed |  |
|  | SUBS_NUMBER | varchar(32) | 32 | NULL allowed |  |
|  | PRODUCT_TYPE | decimal(28,0) | 13 | NULL allowed |  |
|  | EVENT_PARAMETER1 | varchar(4000) | 4000 | NULL allowed |  |
|  | SL_SEIZE_TIME | datetime | 8 | NULL allowed |  |
|  | ORIGINATE_TIME | datetime | 8 | NULL allowed |  |
|  | ANSWER_TIME | datetime | 8 | NULL allowed | _Inicial time of the call_ |
|  | DISCONNECT_TIME | datetime | 8 | NULL allowed | _End time of the call_ |
|  | TRANSACTION_TIME | datetime | 8 | NULL allowed |  |
|  | CHARGEABLE_DURATION | decimal(28,0) | 13 | NULL allowed | _Duration of the call rounded_ |
|  | WALLET_TYPE_ID | int | 4 | NULL allowed |  |
|  | ENDING_BALANCE | decimal(28,6) | 13 | NULL allowed |  |
|  | AMOUNT_CHARGED | decimal(28,6) | 13 | NULL allowed | _Amount charged_ |
|  | PRODUCT_ID | bigint | 8 | NULL allowed |  |
|  | COMMENTS | varchar(4000) | 4000 | NULL allowed |  |
|  | COUNTER_ID | bigint | 8 | NULL allowed |  |
|  | BUNDLE_ID | bigint | 8 | NULL allowed |  |


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

* [dbo].[spc_MovexDRsV9Campaigns]
* [dbo].[spc_MovexDRsV9CampaignsV2]
* [dbo].[spc_ProcessV9Campaigns]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

