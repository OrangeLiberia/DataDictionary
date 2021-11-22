#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccRateTableChamadas

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccRateTableChamadas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccRateTableChamadas: RateTableChamadasID](../../../../Images/pkcluster.png)](#indexes) | RateTableChamadasID | int | 4 | NOT NULL |
|  | RateTableID | int | 4 | NOT NULL |
|  | TierTempoInicio | varchar(4) | 4 | NOT NULL |
|  | TierTempoFim | varchar(4) | 4 | NOT NULL |
|  | PeriodoInicial | int | 4 | NOT NULL |
|  | RateInicial | float | 8 | NOT NULL |
|  | RateIniUnid | float | 8 | NOT NULL |
|  | PeriodoBilling | int | 4 | NOT NULL |
|  | RateBilling | float | 8 | NOT NULL |
|  | RateBillUnid | float | 8 | NOT NULL |
|  | UnidPeriodo | varchar(3) | 3 | NOT NULL |
|  | UnidRate | varchar(3) | 3 | NOT NULL |
|  | TipoAgrava | tinyint | 1 | NULL allowed |
|  | AgravaValor | float | 8 | NULL allowed |
|  | TipoDia | char(2) | 2 | NOT NULL |
|  | TipoHorario | tinyint | 1 | NOT NULL |
|  | INTarifCode | int | 4 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | PriceableItemID | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

