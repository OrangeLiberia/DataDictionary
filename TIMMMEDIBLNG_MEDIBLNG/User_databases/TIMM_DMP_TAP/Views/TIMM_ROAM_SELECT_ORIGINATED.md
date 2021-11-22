#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.TIMM_ROAM_SELECT_ORIGINATED

# ![Views](../../../../Images/View32.png) [dbo].[TIMM_ROAM_SELECT_ORIGINATED]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| BatchID | bigint | 8 |
| ID | int | 4 |
| idoperator | varchar(6) | 6 |
| idoperatordest | bigint | 8 |
| IDAgreement | bigint | 8 |
| A_MSISDN | varchar(32) | 32 |
| A_IMSI | varchar(32) | 32 |
| A_IMEI | varchar(32) | 32 |
| A_CC | varchar(6) | 6 |
| A_NDC | varchar(6) | 6 |
| B_MSISDN | varchar(32) | 32 |
| B_CC | varchar(6) | 6 |
| B_NDC | varchar(6) | 6 |
| Date_Begin_Call | datetime | 8 |
| Date_End_Call | datetime | 8 |
| CallDuration | int | 4 |
| duracao_chamada | varchar(50) | 50 |
| RateValue | numeric(23,10) | 13 |
| RoamingRateValue | numeric(23,10) | 13 |
| PriceableItem | int | 4 |
| periodoMovimento | varchar(6) | 6 |
| IDCountry | smallint | 2 |
| operator | varchar(150) | 150 |
| MCC | varchar(3) | 3 |
| MNC | varchar(3) | 3 |
| CountryCode | varchar(5) | 5 |
| Desig_Completa | varchar(50) | 50 |
| Desig_Abrev | varchar(2) | 2 |
| Tipo | varchar(4) | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

