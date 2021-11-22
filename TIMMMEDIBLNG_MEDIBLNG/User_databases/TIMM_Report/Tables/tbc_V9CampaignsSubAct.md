#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9CampaignsSubAct

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9CampaignsSubAct]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 74724479 |
| Created | 1:35:50 PM Wednesday, December 18, 2019 |
| Last Modified | 11:09:13 AM Wednesday, February 24, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | MSISDN | char(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | OriginateTime | datetime | 8 | NOT NULL | _Date and time of the event_ |
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | ProductID | int | 4 | NOT NULL | _ID of the Product_ |
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | Value | decimal(18,6) | 9 | NOT NULL | _Amount of the transaction_ |
| [![Cluster Key cci_V9CampaignsSubAct: ReferenceDay\BundleID\MSISDN\OriginateTime\ProductID\Value\SubsType](../../../../Images/cluster.png)](#indexes) | SubsType | varchar(5) | 5 | NULL allowed | _Type of the subscriber B2B or B2C_ |


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
* [dbo].[spc_ProcessV9Campaigns]
* [dbo].[tvf_BundlesV9PerMSISDN]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonor]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonorCurrency]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

