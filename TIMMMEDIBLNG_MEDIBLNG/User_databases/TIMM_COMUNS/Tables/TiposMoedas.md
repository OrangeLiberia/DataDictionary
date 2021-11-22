#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TiposMoedas

# ![Tables](../../../../Images/Table32.png) [dbo].[TiposMoedas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PKMOEDAS: IDTipoMoeda](../../../../Images/pkcluster.png)](#indexes) | IDTipoMoeda | int | 4 | NOT NULL | 1 - 1 | NO |
| [![Indexes IX_TiposMoedas](../../../../Images/Index.png)](#indexes) | Cod_ID_Moeda | varchar(12) | 12 | NOT NULL |  |  |
|  | Desig_Completa | varchar(50) | 50 | NOT NULL |  |  |
|  | Desig_Abrev | varchar(20) | 20 | NOT NULL |  |  |
|  | PorDefeito | bit | 1 | NOT NULL |  |  |
|  | DataRegisto | datetime | 8 | NOT NULL |  |  |
|  | IDUtilizador | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |
|  | Design_IMF | varchar(50) | 50 | NULL allowed |  |  |
|  | Desig_Symbol | varchar(5) | 5 | NULL allowed |  |  |
|  | NivelPrioridadePesquisaCambio | tinyint | 1 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

