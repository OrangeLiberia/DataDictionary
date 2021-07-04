#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.PyramidSubsCountMonthly

# ![Tables](../../../../Images/Table32.png) [msc].[PyramidSubsCountMonthly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_PyramidSubsCountMonthly: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_PyramidSubsCountMonthly: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | IDOrigDest | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_PyramidSubsCountMonthly: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | TimeFrameMonths | int | 4 | NOT NULL |  |
|  | NDistinctSubs | int | 4 | NOT NULL | ((0)) |
|  | NBrandNewSubs | int | 4 | NOT NULL | ((0)) |
|  | NZebraSubs | int | 4 | NOT NULL | ((0)) |
|  | NLoyalSubs | int | 4 | NOT NULL | ((0)) |
|  | NComulativeSubs | int | 4 | NOT NULL | ((0)) |
|  | NVLRAttached | int | 4 | NOT NULL | ((0)) |
|  | NVLRRegistered | int | 4 | NOT NULL | ((0)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_PyramidSubsCountMonthly: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | PK_PyramidSubsCountMonthly | IDDimDate, IDOrigDest, TimeFrameMonths | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_GetPyramidMonthly]](../Programmability/Stored_Procedures/spc_GetPyramidMonthly.md)
* [[msc].[spt_LoadPyramidCountersMonthly]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersMonthly.md)
* [[msc].[spt_LoadPyramidCountersMonthlyCU]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersMonthlyCU.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

