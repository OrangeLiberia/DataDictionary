#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Moeda

# ![Tables](../../../../Images/Table32.png) [dbo].[Moeda]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Moeda: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | Codigo | varchar(5) | 5 | NOT NULL |
|  | Designacao | varchar(50) | 50 | NOT NULL |
|  | FK_TCOM_Moeda | int | 4 | NOT NULL |
|  | lastdateupdate | datetime | 8 | NOT NULL |
|  | lastuserupdate | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

