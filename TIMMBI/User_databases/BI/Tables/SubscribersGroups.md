#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubscribersGroups

# ![Tables](../../../../Images/Table32.png) [in].[SubscribersGroups]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubscribersGroups: IDDimDate\IDOrig\MSISDN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubscribersGroups: IDDimDate\IDOrig\MSISDN](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubscribersGroups: IDDimDate\IDOrig\MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |
|  | IDRange | int | 4 | NOT NULL |
|  | Range | varchar(30) | 30 | NULL allowed |
|  | RateBill | float | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubscribersGroups: IDDimDate\IDOrig\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_SubscribersGroups | IDDimDate, IDOrig, MSISDN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[spc_CellcomDevicesDailyUsage]](../../External/Programmability/Stored_Procedures/spc_CellcomDevicesDailyUsage.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_LoadSubscribersGroups]](../Programmability/Stored_Procedures/spc_LoadSubscribersGroups.md)
* [[in].[spt_LoadARPUDistMonthly]](../Programmability/Stored_Procedures/spt_LoadARPUDistMonthly.md)
* [[in].[spt_LoadDistinctSubsARPUDest]](../Programmability/Stored_Procedures/spt_LoadDistinctSubsARPUDest.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

