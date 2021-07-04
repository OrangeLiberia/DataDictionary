#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CellcomDevices

# ![Tables](../../../../Images/Table32.png) [dbo].[CellcomDevices]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevices: IMEI](../../../../Images/pkcluster.png)](#indexes) | IMEI | varchar(20) | 20 | NOT NULL |  |
|  | Model | varchar(100) | 100 | NULL allowed |  |
|  | Inserted | tinyint | 1 | NULL allowed | ((0)) |
|  | InsertDate | datetime | 8 | NULL allowed | (getdate()) |
| [![Foreign Keys FK_CellcomDevices_BatchID: [dbo].[CellcomDevicesBatches].BatchID](../../../../Images/fk.png)](#foreignkeys) | BatchID | smallint | 2 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevices: IMEI](../../../../Images/pkcluster.png)](#indexes) | PK_CellcomDevices | IMEI | YES |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_CellcomDevices_BatchID | BatchID->[[dbo].[CellcomDevicesBatches].[ID]](CellcomDevicesBatches.md) |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

