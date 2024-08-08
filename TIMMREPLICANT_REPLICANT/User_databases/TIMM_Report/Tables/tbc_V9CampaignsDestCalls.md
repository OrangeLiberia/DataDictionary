#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9CampaignsDestCalls

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9CampaignsDestCalls]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 129881 |
| Created | 4:07:16 PM Thursday, December 19, 2019 |
| Last Modified | 2:21:56 AM Friday, January 17, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_V9CampaignsCalls: ReferenceDay\BundleID\ProductType\Destination\Acumulator](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Primary Key PK_tbc_V9CampaignsCalls: ReferenceDay\BundleID\ProductType\Destination\Acumulator](../../../../Images/pk.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
| [![Primary Key PK_tbc_V9CampaignsCalls: ReferenceDay\BundleID\ProductType\Destination\Acumulator](../../../../Images/pk.png)](#indexes) | ProductType | varchar(10) | 10 | NOT NULL | _Type of CDR_ |
| [![Primary Key PK_tbc_V9CampaignsCalls: ReferenceDay\BundleID\ProductType\Destination\Acumulator](../../../../Images/pk.png)](#indexes) | Destination | varchar(20) | 20 | NOT NULL | _Destination type_ |
| [![Primary Key PK_tbc_V9CampaignsCalls: ReferenceDay\BundleID\ProductType\Destination\Acumulator](../../../../Images/pk.png)](#indexes) | Acumulator | varchar(50) | 50 | NOT NULL | _IN Acumulator_ |
|  | NumCalls | bigint | 8 | NULL allowed | _Number of calls_ |
|  | VoiceSeconds | bigint | 8 | NULL allowed | _Total seconds rounded_ |
|  | NumSMS | bigint | 8 | NULL allowed | _Number of SMS_ |
|  | Consumption | bigint | 8 | NULL allowed | _Total MB_ |
|  | AmountCharged | decimal(18,6) | 9 | NULL allowed | _Amount charged as PAYGO_ |


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

* [dbo].[spc_BundleDailyCalls]
* [dbo].[spc_ProcessV9Campaigns]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

