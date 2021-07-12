#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TiposLinguas

# ![Tables](../../../../Images/Table32.png) [dbo].[TiposLinguas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Primary Key PK_LINGUAS: IDTipoLingua](../../../../Images/pk.png)](#indexes) | IDTipoLingua | tinyint | 1 | NOT NULL | 1 - 1 | NO |
| [![Indexes IX_Linguas](../../../../Images/Index.png)](#indexes) | Cod_ID_Lingua | varchar(12) | 12 | NOT NULL |  |  |
|  | Desig_Completa | varchar(50) | 50 | NOT NULL |  |  |
|  | Desig_Abrev | varchar(20) | 20 | NOT NULL |  |  |
|  | PorDefeito | bit | 1 | NOT NULL |  |  |
|  | DataRegisto | datetime | 8 | NOT NULL |  |  |
|  | IDUtilizador | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

