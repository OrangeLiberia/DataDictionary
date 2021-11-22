#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.CallType

# ![Tables](../../../../Images/Table32.png) [fwk].[CallType]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Description |
|---|---|---|---|---|---|---|
|  | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Cluster Primary Key PK_CallType: Type](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
|  | Service | varchar(10) | 10 | NULL allowed |  |  |
|  | MacroType | varchar(50) | 50 | NOT NULL |  |  |
|  | Description | varchar(200) | 200 | NOT NULL |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallType: Type](../../../../Images/pkcluster.png)](#indexes) | PK_CallType | Type | YES | FWK |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[BIDMP_CONSUMPTION_EXPORT]](../../External/Programmability/Stored_Procedures/BIDMP_CONSUMPTION_EXPORT.md)
* [[in].[spc_GetARPUDistMonthlyDetails]](../Programmability/Stored_Procedures/spc_GetARPUDistMonthlyDetails.md)
* [[in].[spc_GetCallsDailyOverview]](../Programmability/Stored_Procedures/spc_GetCallsDailyOverview.md)
* [[in].[spc_GetCallsMonthlyOverview]](../Programmability/Stored_Procedures/spc_GetCallsMonthlyOverview.md)
* [[in].[spc_GetConsumptionDailyOverview]](../Programmability/Stored_Procedures/spc_GetConsumptionDailyOverview.md)
* [[in].[spc_GetConsumptionMonthlyOverview]](../Programmability/Stored_Procedures/spc_GetConsumptionMonthlyOverview.md)
* [[in].[spc_GetGeneralDailyOverview]](../Programmability/Stored_Procedures/spc_GetGeneralDailyOverview.md)
* [[in].[spc_GetWalletBalanceOverview]](../Programmability/Stored_Procedures/spc_GetWalletBalanceOverview.md)
* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

