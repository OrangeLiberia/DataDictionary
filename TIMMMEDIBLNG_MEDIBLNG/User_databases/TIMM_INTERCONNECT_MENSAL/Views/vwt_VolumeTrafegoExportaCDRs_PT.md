#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Views](Views.md) > dbo.vwt_VolumeTrafegoExportaCDRs_PT

# ![Views](../../../../Images/View32.png) [dbo].[vwt_VolumeTrafegoExportaCDRs_PT]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Collation | Max Length (Bytes) |
|---|---|---|---|
| OperadoraID | float |  | 8 |
| Rede | varchar(500) | SQL_Latin1_General_CP1_CI_AS | 500 |
| TipoTrafego | varchar(7) | Latin1_General_CI_AI | 7 |
| Segundos | int |  | 4 |
| ValoraCobrar | float |  | 8 |
| RateporMinuto | float |  | 8 |
| DataInicioChamada | datetime |  | 8 |
| DataFimChamada | datetime |  | 8 |
| NumeroChamador | varchar(32) | Latin1_General_CI_AI | 32 |
| NumeroChamado | varchar(32) | Latin1_General_CI_AI | 32 |
| TrunkEntrada | int |  | 4 |
| RotaEntrada | nvarchar(50) | SQL_Latin1_General_CP1_CI_AS | 100 |
| OperadoraEntrada | nvarchar(255) | SQL_Latin1_General_CP1_CI_AS | 510 |
| TrunkSaida | int |  | 4 |
| RotaSaida | nvarchar(50) | SQL_Latin1_General_CP1_CI_AS | 100 |
| OperadoraSaida | nvarchar(255) | SQL_Latin1_General_CP1_CI_AS | 510 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

