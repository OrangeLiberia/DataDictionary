#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.DimDate

# ![Tables](../../../../Images/Table32.png) [fwk].[DimDate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default | Description |
|---|---|---|---|---|---|---|---|
| [![ PK_DimDateID: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  | Identity of the Date Dimension |
|  | Dt | smalldatetime | 4 | NOT NULL |  |  | Date of reference |
|  | DtDMY | varchar(10) | 10 | NOT NULL |  |  | Date of reference in the format Day-Month-Year |
|  | DtMDY | varchar(10) | 10 | NOT NULL |  |  | Date of reference in the format Month-Day--Year |
|  | DtYMD | varchar(10) | 10 | NOT NULL |  |  | Date of reference in the format Year-Month-Day |
|  | DtYM | varchar(7) | 7 | NOT NULL |  |  | Date of reference in the format Year-Month |
|  | IDPeriodYMD | int | 4 | NOT NULL |  |  | Integer number in the following formula Year*10000 + Month*100 + Day |
|  | IDPeriodYM | int | 4 | NOT NULL |  |  | Integer number in the following formula Year*100 + Month |
|  | IDPeriodY | smallint | 2 | NOT NULL |  |  | Integer number in the following formula Year|
|  | IDWeek | tinyint | 1 | NOT NULL |  |  | Integer number for week number (1 to 54 )|
|  | IDMonth | tinyint | 1 | NOT NULL |  |  | Integer number for month (1 to 12 )|
|  | IDDayOfWeek | tinyint | 1 | NOT NULL |  |  | Integer number for the month (1 Sunday to 7 Saturday )|
|  | IDDayOfMonth | tinyint | 1 | NOT NULL |  |  | Integer number for the day of the month |
|  | IDDayOfYear | smallint | 2 | NOT NULL |  |  | Integer number for the day within a year (1 to 365/366) |
|  | DescDayOfWeek | varchar(20) | 20 | NOT NULL |  |  | Name of the day of the week |
|  | DescMonth | varchar(20) | 20 | NOT NULL |  |  | Name of the month |
|  | IDBimonthly | tinyint | 1 | NOT NULL |  |  |  Integer representing the bi-mester of the Year | 
|  | IDTrimester | tinyint | 1 | NOT NULL |  |  | Integer representing the trimester of the Year  |
|  | IDSemester | tinyint | 1 | NOT NULL |  |  | Integer representing the semester of the Year |
|  | LastDayOfMonth | bit | 1 | NOT NULL |  | ((0)) | Indicates if it's the last day of the month |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DimDateID: ID](../../../../Images/pkcluster.png)](#indexes) | PK_DimDateID | ID | YES | FWK |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[crm].[spc_GetSubscribersMonthlyStats]](../Programmability/Stored_Procedures/spc_GetSubscribersMonthlyStats.md)
* [[crm].[spc_MonthlySnapshot]](../Programmability/Stored_Procedures/spc_MonthlySnapshot.md)
* [[crm].[spc_PrepareCRMViews]](../Programmability/Stored_Procedures/spc_PrepareCRMViews.md)
* [[External].[dbo].[BIDMP_CONSUMPTION_EXPORT]](../../External/Programmability/Stored_Procedures/BIDMP_CONSUMPTION_EXPORT.md)
* [[External].[dbo].[BIDMP_SUBSBASE_EXPORT]](../../External/Programmability/Stored_Procedures/BIDMP_SUBSBASE_EXPORT.md)
* [[External].[dbo].[Report_USIM]](../../External/Programmability/Stored_Procedures/Report_USIM.md)
* [[TIMM_Reports].[dbo].[rpt_RevenuePerSite]](../../TIMM_Reports/Programmability/Stored_Procedures/rpt_RevenuePerSite.md)
* [[TIMM_Reports].[dbo].[Sanza_Campaign]](../../TIMM_Reports/Programmability/Stored_Procedures/Sanza_Campaign.md)
* [[External].[dbo].[spc_AutomaticLTEUpgrade]](../../External/Programmability/Stored_Procedures/spc_AutomaticLTEUpgrade.md)
* [[External].[dbo].[spc_AutomaticSubsSelectionForCleanup]](../../External/Programmability/Stored_Procedures/spc_AutomaticSubsSelectionForCleanup.md)
* [[External].[dbo].[spc_BIStatistics]](../../External/Programmability/Stored_Procedures/spc_BIStatistics.md)
* [[External].[dbo].[spc_CellcomDevicesDailyUsage]](../../External/Programmability/Stored_Procedures/spc_CellcomDevicesDailyUsage.md)
* [[External].[dbo].[spc_GetData75Range]](../../External/Programmability/Stored_Procedures/spc_GetData75Range.md)
* [[External].[dbo].[spc_GetNumberRemainingBalance]](../../External/Programmability/Stored_Procedures/spc_GetNumberRemainingBalance.md)
* [[External].[dbo].[spc_GetOnlineRechargesMonthly]](../../External/Programmability/Stored_Procedures/spc_GetOnlineRechargesMonthly.md)
* [[dbo].[spc_INGetMoneyUsageDistribution]](../Programmability/Stored_Procedures/spc_INGetMoneyUsageDistribution.md)
* [[dbo].[spc_INGetWallet1RevenueSpreadMonthly]](../Programmability/Stored_Procedures/spc_INGetWallet1RevenueSpreadMonthly.md)
* [[External].[dbo].[spc_LoadLDvsUSDReport]](../../External/Programmability/Stored_Procedures/spc_LoadLDvsUSDReport.md)
* [[External].[dbo].[spr_DestinationsByDay]](../../External/Programmability/Stored_Procedures/spr_DestinationsByDay.md)
* [[External].[dbo].[spr_DestinationsByHour]](../../External/Programmability/Stored_Procedures/spr_DestinationsByHour.md)
* [[External].[dbo].[spr_InactiveSubscribersList]](../../External/Programmability/Stored_Procedures/spr_InactiveSubscribersList.md)
* [[TIMM_Reports].[dbo].[spr_KPIOMEARules]](../../TIMM_Reports/Programmability/Stored_Procedures/spr_KPIOMEARules.md)
* [[TIMM_Reports].[dbo].[spr_KPIOrangeMarketShare]](../../TIMM_Reports/Programmability/Stored_Procedures/spr_KPIOrangeMarketShare.md)
* [[External].[dbo].[spr_NewClientsNoTopUpLessFiftyCents]](../../External/Programmability/Stored_Procedures/spr_NewClientsNoTopUpLessFiftyCents.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[fwk].[spc_RunDailyProcess]](../Programmability/Stored_Procedures/spc_RunDailyProcess.md)
* [[fwk].[spt_DatabaseBackupAutomatic]](../Programmability/Stored_Procedures/spt_DatabaseBackupAutomatic.md)
* [[fwk].[spt_ETLRun]](../Programmability/Stored_Procedures/spt_ETLRun.md)
* [[fwk].[spt_TwinTablesBackup]](../Programmability/Stored_Procedures/spt_TwinTablesBackup.md)
* [[in].[_spt_LoadSubsCallsDist_CB]](../Programmability/Stored_Procedures/_spt_LoadSubsCallsDist_CB.md)
* [[in].[_spt_LoadSubsTransactions_CB]](../Programmability/Stored_Procedures/_spt_LoadSubsTransactions_CB.md)
* [[in].[spc_ExtractScratchCardsStock]](../Programmability/Stored_Procedures/spc_ExtractScratchCardsStock.md)
* [[in].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage.md)
* [[in].[spc_LoadScratchCards]](../Programmability/Stored_Procedures/spc_LoadScratchCards.md)
* [[in].[spc_LoadSubscribersGroups]](../Programmability/Stored_Procedures/spc_LoadSubscribersGroups.md)
* [[in].[spc_PrepareXDRViews]](../Programmability/Stored_Procedures/spc_PrepareXDRViews.md)
* [[in].[spc_TransformationScratchCardsDaily]](../Programmability/Stored_Procedures/spc_TransformationScratchCardsDaily.md)
* [[in].[spc_UpdateCustomerEndingBalance]](../Programmability/Stored_Procedures/spc_UpdateCustomerEndingBalance.md)
* [[in].[spt_LoadARPUDistMonthly]](../Programmability/Stored_Procedures/spt_LoadARPUDistMonthly.md)
* [[in].[spt_LoadCallsDist]](../Programmability/Stored_Procedures/spt_LoadCallsDist.md)
* [[in].[spt_LoadCallsDistHourly]](../Programmability/Stored_Procedures/spt_LoadCallsDistHourly.md)
* [[in].[spt_LoadCallsPerCell]](../Programmability/Stored_Procedures/spt_LoadCallsPerCell.md)
* [[in].[spt_LoadDistinctSubsARPUDest]](../Programmability/Stored_Procedures/spt_LoadDistinctSubsARPUDest.md)
* [[in].[spt_LoadScratchCardsTDR]](../Programmability/Stored_Procedures/spt_LoadScratchCardsTDR.md)
* [[in].[spt_LoadSubsCallsDist]](../Programmability/Stored_Procedures/spt_LoadSubsCallsDist.md)
* [[in].[spt_LoadSubsCallsDist_Aux]](../Programmability/Stored_Procedures/spt_LoadSubsCallsDist_Aux.md)
* [[in].[spt_LoadSubsCallsPerCellDevice]](../Programmability/Stored_Procedures/spt_LoadSubsCallsPerCellDevice.md)
* [[in].[spt_LoadSubsScratchCardsTDR]](../Programmability/Stored_Procedures/spt_LoadSubsScratchCardsTDR.md)
* [[in].[spt_LoadSubsTransactions]](../Programmability/Stored_Procedures/spt_LoadSubsTransactions.md)
* [[in].[spt_LoadSubsTransactionsPerCell]](../Programmability/Stored_Procedures/spt_LoadSubsTransactionsPerCell.md)
* [[in].[spt_LoadTransactions]](../Programmability/Stored_Procedures/spt_LoadTransactions.md)
* [[in].[spt_LoadTransactionsPerCell]](../Programmability/Stored_Procedures/spt_LoadTransactionsPerCell.md)
* [[in].[spt_LoadTransferMoneyDist]](../Programmability/Stored_Procedures/spt_LoadTransferMoneyDist.md)
* [[msc].[spc_CallsDailyExportData]](../Programmability/Stored_Procedures/spc_CallsDailyExportData.md)
* [[msc].[spc_CallsDailyExportDataAgg]](../Programmability/Stored_Procedures/spc_CallsDailyExportDataAgg.md)
* [[msc].[spc_CallsDailyExportNRT]](../Programmability/Stored_Procedures/spc_CallsDailyExportNRT.md)
* [[msc].[spc_CallsDailyExportZTE]](../Programmability/Stored_Procedures/spc_CallsDailyExportZTE.md)
* [[msc].[spc_CallsDailyExportZTE_Recover2017]](../Programmability/Stored_Procedures/spc_CallsDailyExportZTE_Recover2017.md)
* [[msc].[spc_GetCallsDistribution]](../Programmability/Stored_Procedures/spc_GetCallsDistribution.md)
* [[msc].[spc_GetPyramidDaily]](../Programmability/Stored_Procedures/spc_GetPyramidDaily.md)
* [[msc].[spc_GetPyramidMonthly]](../Programmability/Stored_Procedures/spc_GetPyramidMonthly.md)
* [[msc].[spc_LoadCellReleaseCauses]](../Programmability/Stored_Procedures/spc_LoadCellReleaseCauses.md)
* [[msc].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_000g.md)
* [[msc].[spc_LoadCustomerUsage_aux]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_aux.md)
* [[msc].[spc_LoadHandsetUsage]](../Programmability/Stored_Procedures/spc_LoadHandsetUsage.md)
* [[msc].[spc_PrepareXDRViews]](../Programmability/Stored_Procedures/spc_PrepareXDRViews_000h.md)
* [[msc].[spc_PrepareXDRViews_aux]](../Programmability/Stored_Procedures/spc_PrepareXDRViews_aux.md)
* [[msc].[spc_UpdateCustomerLastVisitedSite]](../Programmability/Stored_Procedures/spc_UpdateCustomerLastVisitedSite.md)
* [[msc].[spc_UpdateHandsetCustomer]](../Programmability/Stored_Procedures/spc_UpdateHandsetCustomer.md)
* [[msc].[spt_GetPyramidFidelityDaily]](../Programmability/Stored_Procedures/spt_GetPyramidFidelityDaily.md)
* [[msc].[spt_GetPyramidFidelityDailyCU]](../Programmability/Stored_Procedures/spt_GetPyramidFidelityDailyCU.md)
* [[msc].[spt_GetPyramidFidelityMonthly]](../Programmability/Stored_Procedures/spt_GetPyramidFidelityMonthly.md)
* [[msc].[spt_GetPyramidFidelityMonthlyCU]](../Programmability/Stored_Procedures/spt_GetPyramidFidelityMonthlyCU.md)
* [[msc].[spt_LoadCallsDist]](../Programmability/Stored_Procedures/spt_LoadCallsDist_000j.md)
* [[msc].[spt_LoadPyramidCounters]](../Programmability/Stored_Procedures/spt_LoadPyramidCounters.md)
* [[msc].[spt_LoadPyramidCountersCU]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersCU.md)
* [[msc].[spt_LoadPyramidCountersDaily]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersDaily.md)
* [[msc].[spt_LoadPyramidCountersDailyCU]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersDailyCU.md)
* [[msc].[spt_LoadPyramidCountersDailyCU_aux]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersDailyCU_aux.md)
* [[msc].[spt_LoadPyramidCountersMonthly]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersMonthly.md)
* [[msc].[spt_LoadPyramidCountersMonthlyCU]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersMonthlyCU.md)
* [[msc].[spt_LoadPyramidSubs]](../Programmability/Stored_Procedures/spt_LoadPyramidSubs.md)
* [[msc].[spt_LoadSubsCallsDist]](../Programmability/Stored_Procedures/spt_LoadSubsCallsDist_000k.md)
* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)
* [[fwk].[fnt_GetDateFromIDDimDate]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetDateFromIDDimDate.md)
* [[fwk].[fnt_GetIDDimDate]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetIDDimDate.md)
* [[fwk].[fnt_GetPeriodFromIDDimDate]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetPeriodFromIDDimDate.md)
* [[fwk].[fnt_GetVChrDateFromIDDimDate]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetVChrDateFromIDDimDate.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

