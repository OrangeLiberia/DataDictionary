#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CellcomDevicesUsage

# ![Tables](../../../../Images/Table32.png) [dbo].[CellcomDevicesUsage]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevicesUsage: IMEI\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes CellcomDevicesUsage_IX](../../../../Images/Index.png)](#indexes) | IMEI | varchar(20) | 20 | NOT NULL |  |
| [![Cluster Primary Key PK_CellcomDevicesUsage: IMEI\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes CellcomDevicesUsage_IX](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |  |
|  | FirstDay | date | 3 | NOT NULL |  |
|  | LastDay | date | 3 | NOT NULL |  |
|  | FirstTime | bit | 1 | NOT NULL | ((0)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CellcomDevicesUsage: IMEI\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CellcomDevicesUsage | IMEI, MSISDN | YES |
|  | CellcomDevicesUsage_IX | MSISDN, IMEI |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

