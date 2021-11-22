#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CellReleaseCausesDaily2

# ![Tables](../../../../Images/Table32.png) [msc].[CellReleaseCausesDaily2]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CellReleaseCausesDaily2: IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_CellReleaseCausesDaily2: IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | Hour | int |  | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CellReleaseCausesDaily2: IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL |  | _Phone IMEI (imported from msc from aproximated time of CDR)_ |
| [![Cluster Primary Key PK_CellReleaseCausesDaily2: IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | ReleaseCause | smallint |  | 2 | NOT NULL |  |  |
|  | CallDuration | int |  | 4 | NULL allowed | ((0)) | _Duration in seconds_ |
|  | NCallsDur | int |  | 4 | NULL allowed | ((0)) | _Number of calls with duration_ |
|  | NCalls0Dur | int |  | 4 | NULL allowed | ((0)) | _Number of calls with 0 duration_ |
|  | NCalls | int | YES | 4 | NULL allowed |  | _Number of calls_ |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| NCalls | ([NCallsDur]+[NCalls0Dur]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CellReleaseCausesDaily2: IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | PK_CellReleaseCausesDaily2 | IDDimDate, Hour, CellID, ReleaseCause | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[CellReleaseCausesDaily]](../Views/CellReleaseCausesDaily.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_LoadCellReleaseCauses]](../Programmability/Stored_Procedures/spc_LoadCellReleaseCauses.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

