#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CellcomDevicesSubscribersMonthlyUsage

# ![Tables](../../../../Images/Table32.png) [dbo].[CellcomDevicesSubscribersMonthlyUsage]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevicesSubscribersMonthlyUsage: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | Month | date | 3 | NOT NULL |
|  | DayProcessed | date | 3 | NOT NULL |
| [![Cluster Primary Key PK_CellcomDevicesSubscribersMonthlyUsage: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |
|  | IDRange | int | 4 | NOT NULL |
|  | 1Month | bit | 1 | NOT NULL |
|  | 2Month | bit | 1 | NOT NULL |
|  | 3Month | bit | 1 | NOT NULL |
|  | Before3Months | bit | 1 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevicesSubscribersMonthlyUsage: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CellcomDevicesSubscribersMonthlyUsage | IDDimDate, MSISDN | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

