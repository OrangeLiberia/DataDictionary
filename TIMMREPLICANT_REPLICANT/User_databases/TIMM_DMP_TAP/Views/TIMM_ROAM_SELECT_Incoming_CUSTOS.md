#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.TIMM_ROAM_SELECT_Incoming_CUSTOS

# ![Views](../../../../Images/View32.png) [dbo].[TIMM_ROAM_SELECT_Incoming_CUSTOS]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | bigint | 8 |
| sender | varchar(50) | 50 |
| MSISDN | varchar(50) | 50 |
| imsi | varchar(15) | 15 |
| calledNumber | varchar(50) | 50 |
| calledNumber_CC | varchar(10) | 10 |
| calledNumber_NDC | varchar(10) | 10 |
| Date_Begin_Call | datetime | 8 |
| Date_End_Call | datetime | 8 |
| CallDuration | int | 4 |
| chargeableunits | int | 4 |
| chargedUnits | int | 4 |
| charge | numeric(20,6) | 13 |
| localcurrency | varchar(50) | 50 |
| totalcharge | numeric(18,5) | 9 |
| totaltaxvalue | numeric(18,5) | 9 |
| taxvalue | decimal(18,6) | 9 |
| duracao_chamada | varchar(50) | 50 |
| exchangeRate | numeric(18,5) | 9 |
| RoamingType | varchar(10) | 10 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

