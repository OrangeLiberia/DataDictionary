#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Acordos_documento

# ![Tables](../../../../Images/Table32.png) [dbo].[Acordos_documento]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Acordo_documentos: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Acordo_ID | int | 4 | NOT NULL |  |  |
|  | NomeFicheiro | varchar(max) | max | NULL allowed |  |  |
|  | CaminhoFisico | varchar(max) | max | NULL allowed |  |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |  |
|  | deleted | bit | 1 | NOT NULL |  | ((0)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

