#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdDiasFeriado

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdDiasFeriado]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbmdDiasFeriado: DataDoFeriado](../../../../Images/pkcluster.png)](#indexes) | DataDoFeriado | char(10) | 10 | NOT NULL |
|  | Designacao | varchar(100) | 100 | NOT NULL |
|  | TipoDeDia | char(2) | 2 | NOT NULL |
|  | EFeriadoFixo | int | 4 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

