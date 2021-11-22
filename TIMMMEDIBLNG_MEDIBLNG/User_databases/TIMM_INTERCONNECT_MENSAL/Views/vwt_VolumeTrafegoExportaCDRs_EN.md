#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Views](Views.md) > dbo.vwt_VolumeTrafegoExportaCDRs_EN

# ![Views](../../../../Images/View32.png) [dbo].[vwt_VolumeTrafegoExportaCDRs_EN]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Collation | Max Length (Bytes) |
|---|---|---|---|
| OperadoraID | int |  | 4 |
| Rede | varchar(500) | SQL_Latin1_General_CP1_CI_AS | 500 |
| TipoTrafego | varchar(9) | Latin1_General_CI_AI | 9 |
| Segundos | int |  | 4 |
| ValoraCobrar | float |  | 8 |
| RateporMinuto | float |  | 8 |
| DataInicioChamada | datetime |  | 8 |
| DataFimChamada | datetime |  | 8 |
| NumeroChamador | varchar(32) | Latin1_General_CI_AI | 32 |
| NumeroChamado | varchar(32) | Latin1_General_CI_AI | 32 |
| TrunkEntrada | int |  | 4 |
| RotaEntrada | nvarchar(50) | SQL_Latin1_General_CP1_CI_AS | 100 |
| OperadoraEntrada | varchar(200) | SQL_Latin1_General_CP1_CI_AS | 200 |
| TrunkSaida | int |  | 4 |
| RotaSaida | nvarchar(50) | SQL_Latin1_General_CP1_CI_AS | 100 |
| OperadoraSaida | varchar(200) | SQL_Latin1_General_CP1_CI_AS | 200 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

