#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccDescontosPI

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccDescontosPI]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccDescontosPI: DescontoID\PriceableItemID](../../../../Images/pkcluster.png)](#indexes) | DescontoID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccDescontosPI: DescontoID\PriceableItemID](../../../../Images/pkcluster.png)](#indexes) | PriceableItemID | int | 4 | NOT NULL |
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


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

