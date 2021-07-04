#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > orange.TrafficCountersMonthly

# ![Tables](../../../../Images/Table32.png) [orange].[TrafficCountersMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TrafficCountersMonthly: IDDimDate\Service](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | Month | date | 3 | NOT NULL |
| [![Cluster Primary Key PK_TrafficCountersMonthly: IDDimDate\Service](../../../../Images/pkcluster.png)](#indexes) | Service | varchar(20) | 20 | NOT NULL |
|  | NSubs | int | 4 | NOT NULL |
|  | Amount | decimal(10,1) | 9 | NOT NULL |
|  | NCalls | bigint | 8 | NOT NULL |
|  | Units | decimal(10,1) | 9 | NOT NULL |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

