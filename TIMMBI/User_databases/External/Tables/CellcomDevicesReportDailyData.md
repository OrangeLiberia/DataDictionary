#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CellcomDevicesReportDailyData

# ![Tables](../../../../Images/Table32.png) [dbo].[CellcomDevicesReportDailyData]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Indexes IX_CellcomDevicesReportDailyData_PK](../../../../Images/Index.png)](#indexes) | Day | date | 3 | NOT NULL |
| [![Indexes IX_CellcomDevicesReportDailyData_PK](../../../../Images/Index.png)](#indexes) | BatchID | smallint | 2 | NOT NULL |
| [![Indexes IX_CellcomDevicesReportDailyData_PK](../../../../Images/Index.png)](#indexes) | IDRange | int | 4 | NOT NULL |
|  | NDevices | int | 4 | NOT NULL |
|  | NSubscribers | int | 4 | NOT NULL |
|  | BrandNewSubs | int | 4 | NOT NULL |
|  | ActiveSubs | int | 4 | NOT NULL |
|  | ChurnSubs | int | 4 | NOT NULL |
|  | Recharged | decimal(18,2) | 9 | NOT NULL |
|  | Charged | decimal(18,2) | 9 | NOT NULL |
|  | 4GAmount | decimal(18,2) | 9 | NOT NULL |
|  | NDevicesTotal | int | 4 | NOT NULL |
|  | NSubscribersTotal | int | 4 | NOT NULL |
|  | BrandNewSubsTotal | int | 4 | NOT NULL |
|  | ActiveSubsTotal | int | 4 | NOT NULL |
|  | ChurnSubsTotal | int | 4 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_CellcomDevicesReportDailyData_PK | Day, BatchID, IDRange |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

