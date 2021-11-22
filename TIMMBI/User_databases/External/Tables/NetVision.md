#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.NetVision

# ![Tables](../../../../Images/Table32.png) [dbo].[NetVision]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
|  | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Destination | nvarchar(255) | 510 | NOT NULL |  |  |
| [![Cluster Primary Key PK_NetVision_Prefix: Prefix](../../../../Images/pkcluster.png)](#indexes) | Prefix | nvarchar(255) | 510 | NOT NULL |  |  |
|  | Rate | float | 8 | NOT NULL |  |  |
|  | Status | int | 4 | NULL allowed |  | ((0)) |
|  | ParentID | int | 4 | NULL allowed |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_NetVision_Prefix: Prefix](../../../../Images/pkcluster.png)](#indexes) | PK_NetVision_Prefix | Prefix | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

