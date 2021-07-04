#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.CallsOrigDest

# ![Tables](../../../../Images/Table32.png) [fwk].[CallsOrigDest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsDestinations: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |
|  | Name | varchar(20) | 20 | NOT NULL |  |
|  | Description | varchar(250) | 250 | NULL allowed |  |
|  | NameOrig | varchar(20) | 20 | NULL allowed |  |
|  | NameDest | varchar(20) | 20 | NULL allowed |  |
|  | IsGroup | bit | 1 | NOT NULL | ((0)) |
| [![Foreign Keys FK_CallsOrigDest_IDGroup: [fwk].[CallsOrigDest].IDGroup](../../../../Images/fk.png)](#foreignkeys) | IDGroup | int | 4 | NULL allowed |  |
|  | Status | smallint | 2 | NOT NULL | ((1)) |
|  | LastUserID | int | 4 | NOT NULL |  |
|  | LastUpdate | datetime | 8 | NOT NULL | (getdate()) |
|  | Revenue | bit | 1 | NULL allowed | ((0)) |
|  | RevenueAllWallets | bit | 1 | NULL allowed | ((0)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsDestinations: ID](../../../../Images/pkcluster.png)](#indexes) | PK_SubsCallsDestinations | ID | YES | FWK |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_CallsOrigDest_IDGroup | IDGroup->[[fwk].[CallsOrigDest].[ID]]() |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[in].[CallsOrigDestConfig]](CallsOrigDestConfig.md)
* [[msc].[CallsOrigDestConfig]](CallsOrigDestConfig_0003.md)
* [[External].[dbo].[BIDMP_CONSUMPTION_EXPORT]](../../External/Programmability/Stored_Procedures/BIDMP_CONSUMPTION_EXPORT.md)
* [[External].[dbo].[spc_LoadLDvsUSDReport]](../../External/Programmability/Stored_Procedures/spc_LoadLDvsUSDReport.md)
* [[External].[dbo].[spr_DestinationsByDay]](../../External/Programmability/Stored_Procedures/spr_DestinationsByDay.md)
* [[External].[dbo].[spr_DestinationsByHour]](../../External/Programmability/Stored_Procedures/spr_DestinationsByHour.md)
* [[in].[spc_GetARPUDistMonthlyDetails]](../Programmability/Stored_Procedures/spc_GetARPUDistMonthlyDetails.md)
* [[in].[spc_GetCallsDailyDetails]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetails.md)
* [[in].[spc_GetCallsDailyDetailsEx]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetailsEx.md)
* [[in].[spc_GetCallsDailyDetailsExB2B]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetailsExB2B.md)
* [[in].[spc_GetCallsDailyOverview]](../Programmability/Stored_Procedures/spc_GetCallsDailyOverview.md)
* [[in].[spc_GetCallsHourly]](../Programmability/Stored_Procedures/spc_GetCallsHourly.md)
* [[in].[spc_GetCallsMonthlyOverview]](../Programmability/Stored_Procedures/spc_GetCallsMonthlyOverview.md)
* [[in].[spc_GetConsumptionDailyOverview]](../Programmability/Stored_Procedures/spc_GetConsumptionDailyOverview.md)
* [[in].[spc_GetConsumptionMonthlyOverview]](../Programmability/Stored_Procedures/spc_GetConsumptionMonthlyOverview.md)
* [[in].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage.md)
* [[in].[spt_LoadDistinctSubsARPUDest]](../Programmability/Stored_Procedures/spt_LoadDistinctSubsARPUDest.md)
* [[msc].[spc_GetCallsDistribution]](../Programmability/Stored_Procedures/spc_GetCallsDistribution.md)
* [[msc].[spc_GetPyramidDaily]](../Programmability/Stored_Procedures/spc_GetPyramidDaily.md)
* [[msc].[spc_GetPyramidMonthly]](../Programmability/Stored_Procedures/spc_GetPyramidMonthly.md)
* [[msc].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_000g.md)
* [[msc].[spc_LoadCustomerUsage_aux]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_aux.md)
* [[msc].[spc_TransformationCallsDaily]](../Programmability/Stored_Procedures/spc_TransformationCallsDaily_000i.md)
* [[msc].[spt_GetINMSCDailyComparison]](../Programmability/Stored_Procedures/spt_GetINMSCDailyComparison.md)
* [[msc].[spt_GetINMSCMonthlyComparison]](../Programmability/Stored_Procedures/spt_GetINMSCMonthlyComparison.md)
* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)
* [[fwk].[fnt_BelongsToGroup]](../Programmability/Functions/Scalar-valued_Functions/fnt_BelongsToGroup.md)
* [[fwk].[fnt_GetOperatorName]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetOperatorName.md)
* [[fwk].[fnt_GetTopMostGroupID]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetTopMostGroupID.md)
* [[in].[fnt_GetCallOrigDest]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetCallOrigDest.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

