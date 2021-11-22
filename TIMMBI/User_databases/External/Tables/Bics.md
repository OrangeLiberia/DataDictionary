#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.Bics

# ![Tables](../../../../Images/Table32.png) [dbo].[Bics]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Bics: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Code | nvarchar(255) | 510 | NOT NULL |  |  |
| [![Indexes IX_Bics_Destination](../../../../Images/Index.png)](#indexes) | Destination | nvarchar(255) | 510 | NOT NULL |  |  |
|  | Rate | float | 8 | NULL allowed |  |  |
|  | CountryCode | nvarchar(255) | 510 | NOT NULL |  |  |
|  | AreaCode | nvarchar(255) | 510 | NULL allowed |  |  |
| [![Indexes IX_Bics_Prefix](../../../../Images/Index.png)](#indexes) | Prefix | nvarchar(255) | 510 | NOT NULL |  |  |
|  | Index | float | 8 | NOT NULL |  |  |
|  | NetVisionID | int | 4 | NULL allowed |  |  |
|  | Status | int | 4 | NULL allowed |  | ((0)) |
|  | ParentID | int | 4 | NULL allowed |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Bics: ID](../../../../Images/pkcluster.png)](#indexes) | PK_Bics | ID | YES |
|  | IX_Bics_Destination | Destination |  |
|  | IX_Bics_Prefix | Prefix |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

