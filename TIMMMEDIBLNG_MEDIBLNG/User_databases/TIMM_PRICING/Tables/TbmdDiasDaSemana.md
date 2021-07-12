#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdDiasDaSemana

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdDiasDaSemana]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbmdDiasDaSemana: DiaDaSemana](../../../../Images/pkcluster.png)](#indexes) | DiaDaSemana | char(1) | 1 | NOT NULL |
|  | Designacao | varchar(30) | 30 | NOT NULL |
|  | TipoDeDia | char(2) | 2 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

