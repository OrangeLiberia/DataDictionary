#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccPriceableItems

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccPriceableItems]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccPriceableItems: PriceableItemID](../../../../Images/pkcluster.png)](#indexes) | PriceableItemID | int | 4 | NOT NULL |
|  | PriceableItemCod | varchar(12) | 12 | NOT NULL |
|  | EANCod | varchar(50) | 50 | NULL allowed |
|  | PriceableDesc | varchar(200) | 200 | NOT NULL |
|  | CreditDebt | tinyint | 1 | NOT NULL |
|  | PriceableAbrv | varchar(50) | 50 | NULL allowed |
|  | RateTableCod | varchar(12) | 12 | NULL allowed |
|  | PICategoria | tinyint | 1 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | DataEfectiva | datetime | 8 | NOT NULL |
|  | Imposto | int | 4 | NULL allowed |
|  | TipoPI | tinyint | 1 | NOT NULL |
|  | GrupoPI | int | 4 | NOT NULL |
|  | ControloIN | tinyint | 1 | NULL allowed |
|  | ProRata | tinyint | 1 | NOT NULL |
|  | IncDesc | tinyint | 1 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | Vcredito | tinyint | 1 | NULL allowed |
|  | GrupoPIContab | int | 4 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | tipoProduto | nchar(10) | 20 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

