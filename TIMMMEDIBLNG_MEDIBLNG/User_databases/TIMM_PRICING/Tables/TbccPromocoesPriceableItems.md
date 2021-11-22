#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccPromocoesPriceableItems

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccPromocoesPriceableItems]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccPromocoes1: PromocoesID\PriceableItemID](../../../../Images/pkcluster.png)](#indexes) | PromocoesID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccPromocoes1: PromocoesID\PriceableItemID](../../../../Images/pkcluster.png)](#indexes) | PriceableItemID | int | 4 | NOT NULL |
|  | PercDesconto | float | 8 | NULL allowed |
|  | RateTableCod | varchar(12) | 12 | NULL allowed |
|  | PIPromo | int | 4 | NULL allowed |
|  | TCPromo | varchar(10) | 10 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

