#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TiposEntidades

# ![Tables](../../../../Images/Table32.png) [dbo].[TiposEntidades]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Primary Key PK_TiposEntidades: IDTipoEntidade](../../../../Images/pk.png)](#indexes) | IDTipoEntidade | int | 4 | NOT NULL | 1 - 1 | NO |
|  | Cod_Tip_Entidade | varchar(12) | 12 | NOT NULL |  |  |
|  | Desc_Tip_Entidade | varchar(50) | 50 | NOT NULL |  |  |
|  | PorDefeito | bit | 1 | NOT NULL |  |  |
|  | DataRegisto | datetime | 8 | NOT NULL |  |  |
|  | IDUtilizador | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

