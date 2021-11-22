#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9CampaignsDestCallsSubs

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9CampaignsDestCallsSubs]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 1273053803 |
| Created | 4:07:20 PM Thursday, December 19, 2019 |
| Last Modified | 11:12:25 PM Wednesday, December 2, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | MSISDN | char(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | ProductType | varchar(10) | 10 | NOT NULL | _Type of CDR_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | Destination | varchar(20) | 20 | NOT NULL | _Destination type_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | Acumulator | varchar(50) | 50 | NOT NULL | _IN Acumulator_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | NumCalls | bigint | 8 | NULL allowed | _Number of calls_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | VoiceSeconds | bigint | 8 | NULL allowed | _Total seconds rounded_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | NumSMS | bigint | 8 | NULL allowed | _Number of SMS_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | Consumption | bigint | 8 | NULL allowed | _Total MB_ |
| [![Cluster Key cci_V9CampaignsDestCallsSubs: ReferenceDay\BundleID\MSISDN\ProductType\Destination\Acumulator\NumCalls\VoiceSeconds\NumSMS\Consumption\AmountCharged](../../../../Images/cluster.png)](#indexes) | AmountCharged | decimal(18,6) | 9 | NULL allowed | _Amount charged as PAYGO_ |


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

* [[dbo].[vwt_BundlesV9PerMSISDN]](../Views/vwt_BundlesV9PerMSISDN.md)
* [[dbo].[vwt_BundlesV9PerMSISDNAndDonor]](../Views/vwt_BundlesV9PerMSISDNAndDonor.md)
* [dbo].[spc_PAYGDailyARPURevenue]
* [dbo].[spc_PAYGDailyDetails]
* [dbo].[spc_PAYGMonthlyPyramid]
* [dbo].[spc_ProcessV9Campaigns]
* [dbo].[tvf_BundlesV9PerMSISDN]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonor]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonorCurrency]
* [TIMM_Reports].[dbo].[PAYGTop20Daily]
* [TIMM_Reports].[dbo].[PAYGTop20Monthly]
* [TIMM_Reports].[dbo].[TDDB2CConsumption]
* [TIMM_Reports].[dbo].[UNDPDataUsage]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

