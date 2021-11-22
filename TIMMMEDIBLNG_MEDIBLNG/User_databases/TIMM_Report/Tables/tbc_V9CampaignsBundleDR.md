#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9CampaignsBundleDR

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9CampaignsBundleDR]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 821101892 |
| Created | 1:24:10 PM Wednesday, December 18, 2019 |
| Last Modified | 9:10:51 AM Saturday, April 10, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | Action | tinyint | 1 | NOT NULL | _8 - activation, 24 - deactivation_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | Event_Date | datetime | 8 | NOT NULL | _Date and time of the event_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | Activation_Date | datetime | 8 | NOT NULL | _Date and time of the Bundle Activation_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | Expiration_Date | datetime | 8 | NOT NULL | _Date and time of the Bundle deactivation_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | BillingNumber | varchar(9) | 9 | NULL allowed | _MSISDN donor who paid for the bundle_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | Channel | varchar(20) | 20 | NULL allowed | _Channel/source of the activation_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | BundleCost_old | decimal(18,6) | 9 | NULL allowed |  |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | TypeActivation | varchar(100) | 100 | NULL allowed | _Type of the activation_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | CounterStart | varchar(100) | 100 | NULL allowed | _Initial counter value_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | ValidityDays | varchar(100) | 100 | NULL allowed | _Validity Days of the bundle_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | TransactionInfo | varchar(100) | 100 | NULL allowed | _Transaction ID to find linked TDRs and BundleDR_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | COS_ID | int | 4 | NULL allowed | _IN COS ID of the Subscriber_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | SubsType | varchar(5) | 5 | NULL allowed | _Type of the subscriber B2B or B2C_ |
| [![Cluster Key cci_V9CampaignsBundleDR: ReferenceDay\BundleID\MSISDN\Action\Event_Date\Activation_Date\Expiration_Date\BillingNumber\Channel\BundleCost_old\TypeActivation\CounterStart\ValidityDays\TransactionInfo\COS_ID\SubsType\BundleCost](../../../../Images/cluster.png)](#indexes) | BundleCost | varchar(20) | 20 | NULL allowed | _Configured IN cost of the bundle_ |


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
* [[dbo].[vwt_BundlesV9PerMSISDN_NEW]](../Views/vwt_BundlesV9PerMSISDN_NEW.md)
* [[dbo].[vwt_BundlesV9PerMSISDNAndDonor]](../Views/vwt_BundlesV9PerMSISDNAndDonor.md)
* [dbo].[spc_BundleDailyChannelActivations]
* [dbo].[spc_BundleDailyDetailsChanges]
* [dbo].[spc_BundleDailyDonnors]
* [dbo].[spc_BundleDailyDonnorsSummary]
* [dbo].[spc_BundleMonthlyPyramid]
* [dbo].[spc_ProcessV9Campaigns]
* [dbo].[spc_V9BundleExpiration]
* [dbo].[tvf_BundlesV9PerMSISDN]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonor]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonorCurrency]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

