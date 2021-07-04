#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ARPURanges

# ![Tables](../../../../Images/Table32.png) [in].[ARPURanges]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ARPURanges: IDRange](../../../../Images/pkcluster.png)](#indexes) | IDRange | int | 4 | NOT NULL |
|  | Range | varchar(20) | 20 | NOT NULL |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

