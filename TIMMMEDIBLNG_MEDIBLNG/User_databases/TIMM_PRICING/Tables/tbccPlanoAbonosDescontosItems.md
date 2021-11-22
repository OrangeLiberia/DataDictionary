#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.tbccPlanoAbonosDescontosItems

# ![Tables](../../../../Images/Table32.png) [dbo].[tbccPlanoAbonosDescontosItems]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tbccPlanoAbonosDescontosItems: IDPlanoAD\IDSequencia](../../../../Images/pkcluster.png)](#indexes) | IDPlanoAD | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_tbccPlanoAbonosDescontosItems: IDPlanoAD\IDSequencia](../../../../Images/pkcluster.png)](#indexes) | IDSequencia | int | 4 | NOT NULL |
|  | PriceableItemID | int | 4 | NOT NULL |
|  | Valor | decimal(9,2) | 5 | NOT NULL |
|  | QtCiclos | int | 4 | NOT NULL |
|  | LastUpdate | smalldatetime | 4 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

