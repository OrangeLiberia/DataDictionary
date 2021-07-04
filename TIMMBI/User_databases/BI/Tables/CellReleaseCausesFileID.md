#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CellReleaseCausesFileID

# ![Tables](../../../../Images/Table32.png) [msc].[CellReleaseCausesFileID]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CellReleaseCausesFileID: FileID\IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint |  | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_CellReleaseCausesFileID: FileID\IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CellReleaseCausesFileID: FileID\IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | Hour | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CellReleaseCausesFileID: FileID\IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CellReleaseCausesFileID: FileID\IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | ReleaseCause | smallint |  | 2 | NOT NULL |  |
|  | CallDuration | int |  | 4 | NULL allowed | ((0)) |
|  | NCallsDur | int |  | 4 | NULL allowed | ((0)) |
|  | NCalls0Dur | int |  | 4 | NULL allowed | ((0)) |
|  | NCalls | int | YES | 4 | NULL allowed |  |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| NCalls | ([NCallsDur]+[NCalls0Dur]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CellReleaseCausesFileID: FileID\IDDimDate\Hour\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | PK_CellReleaseCausesFileID | FileID, IDDimDate, Hour, CellID, ReleaseCause | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

