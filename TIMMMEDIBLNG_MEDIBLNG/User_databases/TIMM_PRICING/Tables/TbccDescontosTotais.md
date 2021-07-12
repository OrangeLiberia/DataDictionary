#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccDescontosTotais

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccDescontosTotais]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccDescontosTotais: DescontoID](../../../../Images/pkcluster.png)](#indexes) | DescontoID | int | 4 | NOT NULL |
|  | CriterioAtribuicao | tinyint | 1 | NOT NULL |
|  | AcimaLimite | int | 4 | NULL allowed |
|  | CriterioIncidencia | tinyint | 1 | NOT NULL |
|  | Intervalo | int | 4 | NULL allowed |
|  | FormaAtribDesc | tinyint | 1 | NOT NULL |
|  | ValQtdPercTempo | int | 4 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | DataEfectiva | datetime | 8 | NULL allowed |
|  | Status | tinyint | 1 | NULL allowed |
|  | AgenciaFilialID | numeric(18,0) | 9 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | TipoPI | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

