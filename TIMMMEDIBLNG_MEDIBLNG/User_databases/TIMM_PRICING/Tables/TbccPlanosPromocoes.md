#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccPlanosPromocoes

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccPlanosPromocoes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccPlanosPromocoes: PromocoesID](../../../../Images/pkcluster.png)](#indexes) | PromocoesID | int | 4 | NOT NULL | 1 - 1 | NO |
|  | PromocoesDesc | varchar(100) | 100 | NOT NULL |  |  |
|  | TipoServico | int | 4 | NOT NULL |  |  |
|  | DataInicio | datetime | 8 | NOT NULL |  |  |
|  | DataFim | datetime | 8 | NOT NULL |  |  |
|  | TipoPromocao | varchar(1) | 1 | NOT NULL |  |  |
|  | PriceableItemID | int | 4 | NULL allowed |  |  |
|  | Status | int | 4 | NOT NULL |  |  |
|  | DataStatus | datetime | 8 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

