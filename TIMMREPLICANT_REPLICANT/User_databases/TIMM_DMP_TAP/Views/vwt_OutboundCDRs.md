#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vwt_OutboundCDRs

# ![Views](../../../../Images/View32.png) [dbo].[vwt_OutboundCDRs]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| BatchID | bigint | 8 |
| idoperator | int | 4 |
| sender | varchar(50) | 50 |
| MSISDN | varchar(50) | 50 |
| imsi | varchar(15) | 15 |
| imei | varchar(12) | 12 |
| msisdn_CC | varchar(10) | 10 |
| msisdn_NDC | varchar(10) | 10 |
| calledNumber | varchar(50) | 50 |
| calledNumber_CC | varchar(10) | 10 |
| calledNumber_NDC | varchar(10) | 10 |
| Date_Begin_Call | datetime | 8 |
| Date_End_Call | datetime | 8 |
| totalCallEventDuration | int | 4 |
| chargeableunits | int | 4 |
| chargedUnits | int | 4 |
| charge | decimal(18,6) | 9 |
| localcurrency | varchar(50) | 50 |
| totalcharge | numeric(18,5) | 9 |
| totaltaxvalue | numeric(18,5) | 9 |
| taxvalue | decimal(18,6) | 9 |
| duracao_chamada | varchar(50) | 50 |
| exchangeRate | numeric(18,5) | 9 |
| IDCountry | smallint | 2 |
| operator | varchar(150) | 150 |
| MCC | varchar(3) | 3 |
| MNC | varchar(3) | 3 |
| CC | varchar(5) | 5 |
| Desig_Completa | varchar(50) | 50 |
| Alfa_Pais | varchar(2) | 2 |
| RoamingType | varchar(10) | 10 |
| Tipo | varchar(50) | 50 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

