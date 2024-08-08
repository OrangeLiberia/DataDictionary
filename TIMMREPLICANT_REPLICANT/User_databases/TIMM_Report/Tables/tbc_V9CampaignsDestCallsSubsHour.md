#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9CampaignsDestCallsSubsHour

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9CampaignsDestCallsSubsHour]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 14512723 |
| Created | 8:37:23 PM Wednesday, July 1, 2020 |
| Last Modified | 8:37:23 PM Wednesday, July 1, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | MSISDN | char(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | ProductType | varchar(10) | 10 | NOT NULL | _Type of CDR_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | Destination | varchar(20) | 20 | NOT NULL | _Destination type_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | Acumulator | varchar(50) | 50 | NOT NULL | _IN Acumulator_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | Free | tinyint | 1 | NOT NULL | _If it was free or not_ |
| [![Primary Key PK_tbc_V9CampaignsCallsSubsHour: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\Free\Hour](../../../../Images/pk.png)](#indexes) | Hour | tinyint | 1 | NOT NULL | _If the bundle will be processed hourly for hourly reports_ |
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

* [dbo].[spc_BundleDailyDetailsHours]
* [dbo].[spc_BundleDailyDetailsHoursMinutesOffPeak]
* [dbo].[spc_BundleDailyDetailsHoursMinutesPeak]
* [dbo].[spc_BundleDailyDetailsHoursPerHour]
* [dbo].[spc_ProcessV9Campaigns]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

