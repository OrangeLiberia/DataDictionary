#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.ErrorCodes

# ![Tables](../../../../Images/Table32.png) [dbo].[ErrorCodes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Indexes IX_ErrorCodes_IDApp](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Indexes IX_ErrorCodes_IDApp](../../../../Images/Index.png)](#indexes) | Operation | varchar(50) | 50 | NULL allowed |
|  | Description | varchar(1000) | 1000 | NOT NULL |
| [![Cluster Primary Key PK_ErrorCodes: IDApp](../../../../Images/pkcluster.png)](#indexes) | IDApp | int | 4 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ErrorCodes: IDApp](../../../../Images/pkcluster.png)](#indexes) | PK_ErrorCodes | IDApp | YES |
|  | IX_ErrorCodes_IDApp | ID, Operation |  |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

