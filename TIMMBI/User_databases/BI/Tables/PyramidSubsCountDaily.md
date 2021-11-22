#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.PyramidSubsCountDaily

# ![Tables](../../../../Images/Table32.png) [msc].[PyramidSubsCountDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_PyramidSubsCountDaily: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_PyramidSubsCountDaily: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | IDOrigDest | int | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_PyramidSubsCountDaily: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | TimeFrameMonths | int | 4 | NOT NULL |  |  |
|  | NDistinctSubs | int | 4 | NOT NULL | ((0)) |  |
|  | NBrandNewSubs | int | 4 | NOT NULL | ((0)) |  |
|  | NZebraSubs | int | 4 | NOT NULL | ((0)) |  |
|  | NLoyalSubs | int | 4 | NOT NULL | ((0)) |  |
|  | NComulativeSubs | int | 4 | NOT NULL | ((0)) |  |
|  | NVLRAttached | int | 4 | NOT NULL | ((0)) |  |
|  | NVLRRegistered | int | 4 | NOT NULL | ((0)) |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_PyramidSubsCountDaily: IDDimDate\IDOrigDest\TimeFrameMonths](../../../../Images/pkcluster.png)](#indexes) | PK_PyramidSubsCountDaily | IDDimDate, IDOrigDest, TimeFrameMonths | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_GetPyramidDaily]](../Programmability/Stored_Procedures/spc_GetPyramidDaily.md)
* [[msc].[spt_LoadPyramidCountersDaily]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersDaily.md)
* [[msc].[spt_LoadPyramidCountersDailyCU]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersDailyCU.md)
* [[msc].[spt_LoadPyramidCountersDailyCU_aux]](../Programmability/Stored_Procedures/spt_LoadPyramidCountersDailyCU_aux.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

