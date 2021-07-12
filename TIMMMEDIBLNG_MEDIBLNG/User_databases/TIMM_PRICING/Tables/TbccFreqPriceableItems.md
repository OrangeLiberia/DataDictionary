#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccFreqPriceableItems

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccFreqPriceableItems]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccFreqPriceableItems: FrequentesID\PriceableItemID\RateTableCod](../../../../Images/pkcluster.png)](#indexes) | FrequentesID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccFreqPriceableItems: FrequentesID\PriceableItemID\RateTableCod](../../../../Images/pkcluster.png)](#indexes) | PriceableItemID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccFreqPriceableItems: FrequentesID\PriceableItemID\RateTableCod](../../../../Images/pkcluster.png)](#indexes) | RateTableCod | varchar(12) | 12 | NOT NULL |
|  | PIFreq | int | 4 | NOT NULL |
|  | TCFreq | varchar(10) | 10 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

