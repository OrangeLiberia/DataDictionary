#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9VASSubActWallet

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9VASSubActWallet]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 785507 |
| Created | 9:24:17 AM Wednesday, July 1, 2020 |
| Last Modified | 4:11:10 PM Monday, June 21, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| TDRID | int | 4 | NOT NULL | _ID of the TDR (see [dbo.tbc_TDRID](tbc_TDRID.md))_ |
| MSISDN | char(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| OriginateTime | datetime | 8 | NOT NULL | _Date and time of the event_ |
| Value | decimal(18,6) | 9 | NOT NULL | _Amount of the transaction_ |
| ClearCause | varchar(10) | 10 | NOT NULL | _Clear Cause of the transaction_ |
| WALLET_TYPE | int | 4 | NOT NULL | _IN Wallet type_ |


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

* [dbo].[spc_ProcessV9VAS]
* [dbo].[spc_VASDailyDetailsSubsWallet]
* [dbo].[spc_VASOFCDailyDetailsWallet]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

