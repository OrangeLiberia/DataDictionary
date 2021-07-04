#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CellcomDevicesBatches

# ![Tables](../../../../Images/Table32.png) [dbo].[CellcomDevicesBatches]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevicesBatches: ID](../../../../Images/pkcluster.png)](#indexes) | ID | smallint | 2 | NOT NULL | 1 - 1 |
|  | BatchName | varchar(200) | 200 | NOT NULL |  |
|  | InsertDate | datetime | 8 | NOT NULL |  |
|  | Model | varchar(100) | 100 | NOT NULL |  |
|  | NDevices | int | 4 | NOT NULL |  |
|  | CampaignID | int | 4 | NULL allowed |  |
|  | ProductID | int | 4 | NULL allowed |  |
|  | SMS | varchar(200) | 200 | NULL allowed |  |
|  | ProductID2 | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevicesBatches: ID](../../../../Images/pkcluster.png)](#indexes) | PK_CellcomDevicesBatches | ID | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

