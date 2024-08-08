#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdNumerosEspeciaisNDCs

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdNumerosEspeciaisNDCs]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TbmdNumerosEspeciaisNDCs: IDNumeroEspecialNDC](../../../../Images/pkcluster.png)](#indexes) | IDNumeroEspecialNDC | int | 4 | NOT NULL | 1 - 1 | NO |
|  | Codigo | varchar(50) | 50 | NOT NULL |  |  |
|  | CodNDC | int | 4 | NOT NULL |  |  |
|  | DataInicio | datetime | 8 | NOT NULL |  |  |
|  | DataFim | datetime | 8 | NULL allowed |  |  |
|  | DataRegisto | datetime | 8 | NOT NULL |  |  |
|  | IDAccount | int | 4 | NOT NULL |  |  |
|  | Status | bit | 1 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

