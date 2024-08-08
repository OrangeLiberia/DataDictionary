#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vwtb_Inbound_CDRs

# ![Views](../../../../Images/View32.png) [dbo].[vwtb_Inbound_CDRs]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| BatchID | bigint | 8 |
| ID | int | 4 |
| IDAgreement | bigint | 8 |
| Type | varchar(4) | 4 |
| A_MSISDN | varchar(32) | 32 |
| A_IMSI | varchar(32) | 32 |
| A_IMEI | varchar(32) | 32 |
| B_MSISDN | varchar(32) | 32 |
| Date_Begin_Call | datetime | 8 |
| Date_End_Call | datetime | 8 |
| CallDuration | int | 4 |
| RateValue | numeric(23,10) | 13 |
| RoamingRateValue | numeric(23,10) | 13 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

