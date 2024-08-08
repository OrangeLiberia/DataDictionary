#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomTipoServico

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomTipoServico]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomTipoServico: TipoServico](../../../../Images/pkcluster.png)](#indexes) | TipoServico | tinyint | 1 | NOT NULL |
|  | TipoServicoDesc | varchar(50) | 50 | NOT NULL |
|  | AreaNegocioID | numeric(18,0) | 9 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | Activo | bit | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

