#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9VAS

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9VAS]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 29530 |
| Created | 1:43:22 PM Thursday, January 30, 2020 |
| Last Modified | 1:43:22 PM Thursday, January 30, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_V9VAS: ReferenceDay\TDRID](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Primary Key PK_tbc_V9VAS: ReferenceDay\TDRID](../../../../Images/pk.png)](#indexes) | TDRID | int | 4 | NOT NULL | _ID of the TDR (see [dbo.tbc_TDRID](tbc_TDRID.md))_ |
|  | PaidActivationsP | int | 4 | NULL allowed | _Number of positive transactions_ |
|  | PaidActivationsN | int | 4 | NULL allowed | _Number of negative transactions_ |
|  | FreeActivations | int | 4 | NULL allowed | _Number of free transactions_ |
|  | FreeActivationsNoBalance | int | 4 | NULL allowed | _Number of no balance transactions_ |
|  | FeeP | decimal(18,6) | 9 | NULL allowed | _Total amount positive_ |
|  | FeeN | decimal(18,6) | 9 | NULL allowed | _Total amount negative_ |
|  | ZebraSubs | int | 4 | NOT NULL | _Total Zebras subscribers_ |
|  | ChurnedSubs | int | 4 | NOT NULL | _Total Churned subscribers_ |
|  | BrandNewSubs | int | 4 | NOT NULL | _Total Brand new subscribers_ |


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
* [dbo].[spc_VASDailyDetails]
* [dbo].[spc_VASMonthlyFee]
* [dbo].[spc_VASOFCDailyDetailsWallet]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

