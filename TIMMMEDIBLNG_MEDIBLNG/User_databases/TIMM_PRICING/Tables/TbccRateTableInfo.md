#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccRateTableInfo

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccRateTableInfo]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccRateTableInfo: RateTableID](../../../../Images/pkcluster.png)](#indexes) | RateTableID | int | 4 | NOT NULL |
|  | RateTableCod | varchar(12) | 12 | NOT NULL |
|  | RateTableDesc | varchar(200) | 200 | NOT NULL |
|  | RateTableAbrv | varchar(50) | 50 | NULL allowed |
|  | Status | tinyint | 1 | NOT NULL |
|  | DataStatus | datetime | 8 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | TipoServico | tinyint | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

