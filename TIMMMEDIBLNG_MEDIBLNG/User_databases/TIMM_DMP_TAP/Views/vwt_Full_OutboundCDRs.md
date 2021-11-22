#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vwt_Full_OutboundCDRs

# ![Views](../../../../Images/View32.png) [dbo].[vwt_Full_OutboundCDRs]

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
| imsi | varchar(32) | 32 |
| imei | varchar(32) | 32 |
| msisdn_CC | varchar(10) | 10 |
| msisdn_NDC | varchar(10) | 10 |
| calledNumber | varchar(65) | 65 |
| calledNumber_CC | varchar(10) | 10 |
| calledNumber_NDC | varchar(10) | 10 |
| Date_Begin_Call | datetime | 8 |
| Date_End_Call | datetime | 8 |
| totalCallEventDuration | int | 4 |
| DataVolumeIncoming | bigint | 8 |
| DataVolumeOutgoing | bigint | 8 |
| chargeableunits | bigint | 8 |
| chargedUnits | bigint | 8 |
| charge | decimal(38,6) | 17 |
| localcurrency | varchar(50) | 50 |
| totalcharge | numeric(18,5) | 9 |
| totaltaxvalue | numeric(18,5) | 9 |
| taxvalue | decimal(38,6) | 17 |
| duracao_chamada | varchar(50) | 50 |
| exchangeRate | numeric(18,5) | 9 |
| IDCountry | smallint | 2 |
| operator | varchar(150) | 150 |
| MCC | varchar(3) | 3 |
| MNC | varchar(3) | 3 |
| CC | varchar(5) | 5 |
| Desig_Completa | varchar(50) | 50 |
| Alfa_Pais | varchar(2) | 2 |
| RoamingType | int | 4 |
| Tipo | varchar(50) | 50 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

