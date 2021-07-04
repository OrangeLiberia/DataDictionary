#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.DistinctSubsARPUDest

# ![Tables](../../../../Images/Table32.png) [in].[DistinctSubsARPUDest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Indexes IX_DistinctSubsARPUDest](../../../../Images/Index.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |
| [![Indexes IX_DistinctSubsARPUDest](../../../../Images/Index.png)](#indexes) | Type | varchar(10) | 10 | NULL allowed |  |
| [![Indexes IX_DistinctSubsARPUDest](../../../../Images/Index.png)](#indexes) | IDDest | int | 4 | NULL allowed |  |
|  | ReportGroup | bit | 1 | NOT NULL | ((0)) |
| [![Indexes IX_DistinctSubsARPUDest](../../../../Images/Index.png)](#indexes) | ReportName | varchar(50) | 50 | NULL allowed |  |
| [![Indexes IX_DistinctSubsARPUDest](../../../../Images/Index.png)](#indexes) | IDRange | int | 4 | NULL allowed |  |
|  | NSubs | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns | File Group |
|---|---|---|
| IX_DistinctSubsARPUDest | IDDimDate, Type, IDDest, ReportName, IDRange | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spt_LoadDistinctSubsARPUDest]](../Programmability/Stored_Procedures/spt_LoadDistinctSubsARPUDest.md)
* [[in].[fnt_GetDistinctSubsARPU]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetDistinctSubsARPU.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

