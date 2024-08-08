#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vwt_InboundCDRs

# ![Views](../../../../Images/View32.png) [dbo].[vwt_InboundCDRs]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Collation | Max Length (Bytes) |
|---|---|---|---|
| BatchID | bigint |  | 8 |
| ID | int |  | 4 |
| idoperator | int |  | 4 |
| idoperatordest | bigint |  | 8 |
| IDAgreement | bigint |  | 8 |
| A_MSISDN | varchar(32) | Latin1_General_CI_AS | 32 |
| A_IMSI | varchar(32) | Latin1_General_CI_AS | 32 |
| A_IMEI | varchar(32) | Latin1_General_CI_AS | 32 |
| A_CC | varchar(7) | Latin1_General_CI_AS | 7 |
| A_NDC | varchar(32) | Latin1_General_CI_AS | 32 |
| B_MSISDN | varchar(65) | Latin1_General_CI_AS | 65 |
| B_CC | varchar(6) | Latin1_General_CI_AS | 6 |
| B_NDC | varchar(6) | Latin1_General_CI_AS | 6 |
| Date_Begin_Call | datetime |  | 8 |
| Date_End_Call | datetime |  | 8 |
| CallDuration | int |  | 4 |
| duracao_chamada | varchar(50) | Latin1_General_CI_AS | 50 |
| RateValue | numeric(23,10) |  | 13 |
| RoamingRateValue | numeric(23,10) |  | 13 |
| PriceableItem | int |  | 4 |
| periodoMovimento | varchar(6) | Latin1_General_CI_AS | 6 |
| IDCountry | smallint |  | 2 |
| operator | varchar(150) | SQL_Latin1_General_CP1_CI_AS | 150 |
| MCC | varchar(3) | SQL_Latin1_General_CP1_CI_AS | 3 |
| MNC | varchar(3) | SQL_Latin1_General_CP1_CI_AS | 3 |
| CountryCode | varchar(5) | SQL_Latin1_General_CP1_CI_AS | 5 |
| Desig_Completa | varchar(50) | SQL_Latin1_General_CP1_CI_AS | 50 |
| Desig_Abrev | varchar(2) | SQL_Latin1_General_CP1_CI_AS | 2 |
| Tipo | varchar(4) | Latin1_General_CI_AS | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

