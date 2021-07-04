#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsLOC02

# ![Tables](../../../../Images/Table32.png) [msc].[CallsLOC02]

---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsLOC02: FileID\ID\LinkedID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_CallsLOC02: FileID\ID\LinkedID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_CallsLOC02: FileID\ID\LinkedID](../../../../Images/pkcluster.png)](#indexes) | LinkedID | int | 4 | NOT NULL |
|  | LocationAreaCode | int | 4 | NULL allowed |
|  | Cell_SAC_ID | int | 4 | NULL allowed |
|  | Date_Time | datetime | 8 | NULL allowed |
|  | MSC | tinyint | 1 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsLOC02: FileID\ID\LinkedID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsLOC02 | FileID, ID, LinkedID | YES | MSC |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

