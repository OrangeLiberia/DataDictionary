#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9Campaigns

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9Campaigns]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 103425 |
| Created | 12:44:07 PM Thursday, December 19, 2019 |
| Last Modified | 12:44:07 PM Thursday, December 19, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_V9Campaigns: ReferenceDay\BundleID](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Primary Key PK_tbc_V9Campaigns: ReferenceDay\BundleID](../../../../Images/pk.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
|  | Activations | int | 4 | NULL allowed | _Number of Activations_ |
|  | Deactivations | int | 4 | NULL allowed | _Number of Deactivations_ |
|  | Renewal | int | 4 | NULL allowed | _Number of Renewals_ |
|  | DistinctActivations | int | 4 | NULL allowed | _Number of Distinct MSISDN that got Activations_ |
|  | DistinctPaidActivations | int | 4 | NULL allowed | _Number of Distinct MSISDN that paid for Activations_ |
|  | FeeUSSD | decimal(18,6) | 9 | NULL allowed | _Total amount paid in IN in USD_ |
|  | FeeOMLRD | decimal(18,6) | 9 | NULL allowed | _Total amount paid in OM in LRD_ |
|  | FeeOMUSD | decimal(18,6) | 9 | NULL allowed | _Total amount paid in OM in USD_ |
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

* [dbo].[spc_BundleDailyDetails]
* [dbo].[spc_BundleDailyDetailsDetailed]
* [dbo].[spc_BundleDailyDetailsHours]
* [dbo].[spc_BundleMonthlyFee]
* [dbo].[spc_ProcessV9Campaigns]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

