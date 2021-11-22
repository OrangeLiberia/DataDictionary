#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccPromocoes

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccPromocoes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccPromocoes: PromocoesID](../../../../Images/pkcluster.png)](#indexes) | PromocoesID | int | 4 | NOT NULL |
|  | PricingPlanID | int | 4 | NOT NULL |
|  | PriceableItemID | int | 4 | NOT NULL |
|  | PercDesconto | float | 8 | NULL allowed |
|  | RateTableCod | varchar(12) | 12 | NULL allowed |
|  | DataInicio | datetime | 8 | NOT NULL |
|  | DataFim | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

