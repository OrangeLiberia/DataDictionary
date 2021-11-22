#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > orange.TrafficCountersMonthly

# ![Tables](../../../../Images/Table32.png) [orange].[TrafficCountersMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TrafficCountersMonthly: IDDimDate\Service](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
|  | Month | date | 3 | NOT NULL |  |
| [![Cluster Primary Key PK_TrafficCountersMonthly: IDDimDate\Service](../../../../Images/pkcluster.png)](#indexes) | Service | varchar(20) | 20 | NOT NULL |  |
|  | NSubs | int | 4 | NOT NULL | _Number of subscribers_ |
|  | Amount | decimal(10,1) | 9 | NOT NULL |  |
|  | NCalls | bigint | 8 | NOT NULL | _Number of calls_ |
|  | Units | decimal(10,1) | 9 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TrafficCountersMonthly: IDDimDate\Service](../../../../Images/pkcluster.png)](#indexes) | PK_TrafficCountersMonthly | IDDimDate, Service | YES |


---

## <a name="#uses"></a>Uses

* [orange]


---

## <a name="#usedby"></a>Used By

* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

