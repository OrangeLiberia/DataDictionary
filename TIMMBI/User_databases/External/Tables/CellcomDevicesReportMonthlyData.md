#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CellcomDevicesReportMonthlyData

# ![Tables](../../../../Images/Table32.png) [dbo].[CellcomDevicesReportMonthlyData]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Indexes IX_CellcomDevicesReportMonthlyData_PK](../../../../Images/Index.png)](#indexes) | Month | date | 3 | NOT NULL |
| [![Indexes IX_CellcomDevicesReportMonthlyData_PK](../../../../Images/Index.png)](#indexes) | BatchID | smallint | 2 | NOT NULL |
| [![Indexes IX_CellcomDevicesReportMonthlyData_PK](../../../../Images/Index.png)](#indexes) | IDRange | int | 4 | NOT NULL |
|  | DayOfProcess | date | 3 | NOT NULL |
|  | NDevices | int | 4 | NOT NULL |
|  | NSubscribers | int | 4 | NOT NULL |
|  | BrandNewSubs | int | 4 | NOT NULL |
|  | ActiveSubs | int | 4 | NOT NULL |
|  | ChurnSubs | int | 4 | NOT NULL |
|  | NDevicesTotal | int | 4 | NOT NULL |
|  | NSubscribersTotal | int | 4 | NOT NULL |
|  | BrandNewSubsTotal | int | 4 | NOT NULL |
|  | ActiveSubsTotal | int | 4 | NOT NULL |
|  | ChurnSubsTotal | int | 4 | NOT NULL |
|  | NDevicesCumulative | int | 4 | NOT NULL |
|  | NSubscribersCumulative | int | 4 | NOT NULL |
|  | BrandNewSubsCumulative | int | 4 | NOT NULL |
|  | ActiveSubsCumulative | int | 4 | NOT NULL |
|  | ChurnSubsCumulative | int | 4 | NOT NULL |
|  | NDevicesCumulativeTotal | int | 4 | NOT NULL |
|  | NSubscribersCumulativeTotal | int | 4 | NOT NULL |
|  | BrandNewSubsCumulativeTotal | int | 4 | NOT NULL |
|  | ActiveSubsCumulativeTotal | int | 4 | NOT NULL |
|  | ChurnSubsCumulativeTotal | int | 4 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_CellcomDevicesReportMonthlyData_PK | Month, BatchID, IDRange |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

