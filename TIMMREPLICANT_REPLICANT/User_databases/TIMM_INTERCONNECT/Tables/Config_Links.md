#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Config_Links

# ![Tables](../../../../Images/Table32.png) [dbo].[Config_Links]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_links: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | tipodelink | nvarchar(50) | 100 | NOT NULL |  |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |  |
|  | deleted | bit | 1 | NOT NULL |  | ((0)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

