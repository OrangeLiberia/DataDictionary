#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vwt_DMP_Repository_ImportedCDRs_Hist_3Y

# ![Views](../../../../Images/View32.png) [dbo].[vwt_DMP_Repository_ImportedCDRs_Hist_3Y]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | bigint | 8 |
| FileDescriptorID | bigint | 8 |
| RoamingType | varchar(10) | 10 |
| imsi | varchar(15) | 15 |
| msisdn | varchar(50) | 50 |
| msisdn_wnpID | int | 4 |
| msisdn_CC | varchar(10) | 10 |
| msisdn_NDC | varchar(10) | 10 |
| msisdn_OrigDest | varchar(10) | 10 |
| calledNumber | varchar(50) | 50 |
| calledNumber_wnpID | int | 4 |
| calledNumber_CC | varchar(10) | 10 |
| calledNumber_NDC | varchar(10) | 10 |
| calledNumber_OrigDest | varchar(10) | 10 |
| localTimeStamp | datetime | 8 |
| utcTimeOffset | varchar(16) | 16 |
| totalCallEventDuration | int | 4 |
| recEntityCode | varchar(50) | 50 |
| callReference | varchar(50) | 50 |
| locationArea | varchar(20) | 20 |
| cellId | int | 4 |
| servingBid | varchar(50) | 50 |
| servingLocationDescription | varchar(50) | 50 |
| teleServiceCode | varchar(2) | 2 |
| chargedItem | varchar(2) | 2 |
| chargeType | varchar(2) | 2 |
| charge | decimal(18,6) | 9 |
| chargeableUnits | int | 4 |
| chargedUnits | int | 4 |
| calledPlace | varchar(20) | 20 |
| calledRegion | varchar(20) | 20 |
| imei | varchar(12) | 12 |
| taxCode | int | 4 |
| taxValue | decimal(18,6) | 9 |
| CAMELServiceLevel | varchar(16) | 16 |
| CAMELServiceKey | int | 4 |
| CAMELtaxCode | int | 4 |
| CAMELtaxValue | decimal(18,6) | 9 |
| CAMELInvocationFee | decimal(18,6) | 9 |
| CAMELexchangeRateCode | int | 4 |
| CAMEL3GDestinationNumber | varchar(32) | 32 |
| CAMELSEInformation | varchar(256) | 256 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

