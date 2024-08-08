#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_TDRID

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_TDRID]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 50 |
| Created | 9:31:28 PM Wednesday, December 25, 2019 |
| Last Modified | 9:42:51 AM Wednesday, July 1, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_TDRID: TDRID](../../../../Images/pk.png)](#indexes) | TDRID | int | 4 | NOT NULL | _ID of the TDR (see [dbo.tbc_TDRID](tbc_TDRID.md))_ |
|  | Name | varchar(100) | 100 | NULL allowed | _Name_ |
|  | Wallet | tinyint | 1 | NULL allowed | _If TK/VAS will be processed by Wallet for wallet reports_ |


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

* [[dbo].[vwt_VASV9PerMSISDN]](../Views/vwt_VASV9PerMSISDN.md)
* [dbo].[spc_ProcessV9VAS]
* [dbo].[spc_TDRID]
* [dbo].[spc_VASDailyARPU]
* [dbo].[spc_VASDailyDetails]
* [dbo].[spc_VASDailyDetailsSubsWallet]
* [dbo].[spc_VASDailyFees]
* [dbo].[spc_VASMonthlyFee]
* [dbo].[spc_VASMonthlyPyramid]
* [dbo].[spc_VASOFCDailyDetailsWallet]
* [TIMM_Reports].[dbo].[VASB2BReport]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

