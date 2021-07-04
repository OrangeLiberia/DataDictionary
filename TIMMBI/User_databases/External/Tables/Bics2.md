#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.Bics2

# ![Tables](../../../../Images/Table32.png) [dbo].[Bics2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Bics2: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_Bics2_Destination](../../../../Images/Index.png)](#indexes) | Destination | nvarchar(255) | 510 | NOT NULL |  |  |
| [![Indexes IX_Bics2_Prefix](../../../../Images/Index.png)](#indexes) | Prefix | nvarchar(255) | 510 | NOT NULL |  |  |
|  | Rate | float | 8 | NULL allowed |  |  |
|  | Status | int | 4 | NULL allowed |  | ((0)) |
|  | ParentID | int | 4 | NULL allowed |  |  |
|  | DestinationOriginal | nvarchar(255) | 510 | NOT NULL |  |  |
|  | CommonDest | varchar(100) | 100 | NULL allowed |  |  |
|  | CommonPrefix | varchar(20) | 20 | NULL allowed |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Bics2: ID](../../../../Images/pkcluster.png)](#indexes) | PK_Bics2 | ID | YES |
|  | IX_Bics2_Destination | Destination |  |
|  | IX_Bics2_Prefix | Prefix |  |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

