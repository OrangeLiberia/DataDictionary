#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.TableSize

# ![Tables](../../../../Images/Table32.png) [dbo].[TableSize]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TableSize: DBNAme\SchemaName\TableName](../../../../Images/pkcluster.png)](#indexes) | DBNAme | nvarchar(50) | 100 | NOT NULL |
| [![Cluster Primary Key PK_TableSize: DBNAme\SchemaName\TableName](../../../../Images/pkcluster.png)](#indexes) | SchemaName | nvarchar(50) | 100 | NOT NULL |
| [![Cluster Primary Key PK_TableSize: DBNAme\SchemaName\TableName](../../../../Images/pkcluster.png)](#indexes) | TableName | nvarchar(100) | 200 | NOT NULL |
|  | DataSpace | float | 8 | NULL allowed |
|  | IndexSpace | float | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TableSize: DBNAme\SchemaName\TableName](../../../../Images/pkcluster.png)](#indexes) | PK_TableSize | DBNAme, SchemaName, TableName | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

