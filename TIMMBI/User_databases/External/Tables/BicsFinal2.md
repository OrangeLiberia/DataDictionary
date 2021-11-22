#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.BicsFinal2

# ![Tables](../../../../Images/Table32.png) [dbo].[BicsFinal2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_BicsFinal2: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Indexes IX_BicsFinal2_Destination](../../../../Images/Index.png)](#indexes) | Destination | varchar(100) | 100 | NOT NULL |
| [![Indexes IX_BicsFinal2_Prefix](../../../../Images/Index.png)](#indexes) | Prefix | varchar(10) | 10 | NOT NULL |
|  | Rate | float | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_BicsFinal2: ID](../../../../Images/pkcluster.png)](#indexes) | PK_BicsFinal2 | ID | YES |
|  | IX_BicsFinal2_Prefix | Prefix | YES |
|  | IX_BicsFinal2_Destination | Destination |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

