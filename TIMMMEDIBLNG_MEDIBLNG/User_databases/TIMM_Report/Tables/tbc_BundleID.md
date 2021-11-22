#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_BundleID

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_BundleID]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 173 |
| Created | 10:19:19 AM Wednesday, December 18, 2019 |
| Last Modified | 8:38:20 PM Wednesday, July 1, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_BundleID: BundleID](../../../../Images/pk.png)](#indexes) | BundleID | int | 4 | NOT NULL | _ID of the Bundle (see [dbo.tbc_BundleID](tbc_BundleID.md))_ |
|  | Name | varchar(100) | 100 | NULL allowed | _Name_ |
|  | ProductID | int | 4 | NULL allowed | _ID of the Product_ |
|  | 4GDataPack | tinyint | 1 | NULL allowed | _If bundle is a 4G data pack_ |
|  | Hour | tinyint | 1 | NULL allowed | _If the bundle will be processed hourly for hourly reports_ |


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

* [[DW_OrangeMoney].[dbo].[vw_BundleConfig]](../../DW_OrangeMoney/Views/vw_BundleConfig.md)
* [[dbo].[vwt_BundlesV9PerMSISDN]](../Views/vwt_BundlesV9PerMSISDN.md)
* [[dbo].[vwt_BundlesV9PerMSISDN_NEW]](../Views/vwt_BundlesV9PerMSISDN_NEW.md)
* [[dbo].[vwt_BundlesV9PerMSISDNAndDonor]](../Views/vwt_BundlesV9PerMSISDNAndDonor.md)
* [dbo].[spc_BundleDailyARPU]
* [dbo].[spc_BundleDailyCalls]
* [dbo].[spc_BundleDailyChannelActivations]
* [dbo].[spc_BundleDailyDetails]
* [dbo].[spc_BundleDailyDetailsBundleRewards]
* [dbo].[spc_BundleDailyDetailsChanges]
* [dbo].[spc_BundleDailyDetailsDetailed]
* [dbo].[spc_BundleDailyDetailsHours]
* [dbo].[spc_BundleDailyDetailsHoursMinutesOffPeak]
* [dbo].[spc_BundleDailyDetailsHoursMinutesPeak]
* [dbo].[spc_BundleDailyDetailsHoursPerHour]
* [dbo].[spc_BundleDailyDonnors]
* [dbo].[spc_BundleDailyDonnorsSummary]
* [dbo].[spc_BundleID]
* [dbo].[spc_BundleMonthlyFee]
* [dbo].[spc_BundleMonthlyPyramid]
* [dbo].[spc_OMAgents]
* [dbo].[spc_OMAgents_Weekly]
* [dbo].[spc_ProcessV9Campaigns]
* [dbo].[spc_TDDCustomers]
* [dbo].[spc_V980PercentBundleSLEEDR]
* [dbo].[spc_V9BundleExpiration]
* [dbo].[tvf_BundlesV9PerMSISDN]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonor]
* [dbo].[tvf_BundlesV9PerMSISDNAndDonorCurrency]
* [TIMM_Reports].[dbo].[buybundlebydealers]
* [TIMM_Reports].[dbo].[buybundletimeseries]
* [TIMM_Reports].[dbo].[buybundletimeseriesweekly]
* [TIMM_Reports].[dbo].[rpt_dailybuybundlereport]
* [TIMM_Reports].[dbo].[spc_buybundledailyanalysis]
* [TIMM_Reports].[dbo].[StoredProcedureName]
* [TIMM_Reports].[dbo].[TDDB2CConsumption]
* [TIMM_Reports].[dbo].[weeklybbl]
* [TIMM_Reports].[dbo].[weeklybblsummary]
* [TIMM_Reports].[dbo].[weeklybblsummarysuperagents]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

