#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TiposImpostos

# ![Tables](../../../../Images/Table32.png) [dbo].[TiposImpostos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_IMPOSTOS: IDTipoImposto](../../../../Images/pkcluster.png)](#indexes) | IDTipoImposto | tinyint | 1 | NOT NULL | 1 - 1 | NO |
| [![Indexes IX_Impostos](../../../../Images/Index.png)](#indexes) | Cod_ID_TipoImposto | varchar(12) | 12 | NOT NULL |  |  |
|  | Desig_Completa | varchar(50) | 50 | NOT NULL |  |  |
|  | Desig_Abrev | varchar(20) | 20 | NOT NULL |  |  |
|  | Perc_Imposto | float | 8 | NOT NULL |  |  |
|  | PorDefeito | bit | 1 | NOT NULL |  |  |
|  | DataRegisto | datetime | 8 | NOT NULL |  |  |
|  | IDUtilizador | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |
|  | PriceableItemID | int | 4 | NULL allowed |  |  |
|  | Incidencia | tinyint | 1 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

