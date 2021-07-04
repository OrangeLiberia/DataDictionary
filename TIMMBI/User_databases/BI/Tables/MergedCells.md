#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.MergedCells

# ![Tables](../../../../Images/Table32.png) [msc].[MergedCells]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_MergedCells: CellID](../../../../Images/pkcluster.png)](#indexes) | CellID | int | 4 | NOT NULL |
|  | NewCellID | varchar(50) | 50 | NULL allowed |
|  | NewSiteName | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_MergedCells: CellID](../../../../Images/pkcluster.png)](#indexes) | PK_MergedCells | CellID | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[CellsSitesLocation]](../Views/CellsSitesLocation.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

