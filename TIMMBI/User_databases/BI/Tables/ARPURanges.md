#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ARPURanges

# ![Tables](../../../../Images/Table32.png) [in].[ARPURanges]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ARPURanges: IDRange](../../../../Images/pkcluster.png)](#indexes) | IDRange | int | 4 | NOT NULL | _ID of the ARPU Range (see [in.ARPURanges](ARPURanges.md))_ |
|  | Range | varchar(20) | 20 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ARPURanges: IDRange](../../../../Images/pkcluster.png)](#indexes) | PK_ARPURanges | IDRange | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[spc_CellcomDevicesDailyUsage]](../../External/Programmability/Stored_Procedures/spc_CellcomDevicesDailyUsage.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

