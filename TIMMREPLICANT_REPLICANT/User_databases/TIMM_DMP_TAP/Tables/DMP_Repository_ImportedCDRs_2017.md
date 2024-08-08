#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_Repository_ImportedCDRs_2017

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_Repository_ImportedCDRs_2017]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| ID | bigint | 8 | NOT NULL | 1 - 1 |
| FileDescriptorID | bigint | 8 | NOT NULL |  |
| RoamingType | varchar(10) | 10 | NULL allowed |  |
| imsi | varchar(15) | 15 | NULL allowed |  |
| msisdn | varchar(50) | 50 | NULL allowed |  |
| msisdn_wnpID | int | 4 | NULL allowed |  |
| msisdn_CC | varchar(10) | 10 | NULL allowed |  |
| msisdn_NDC | varchar(10) | 10 | NULL allowed |  |
| msisdn_OrigDest | varchar(10) | 10 | NULL allowed |  |
| calledNumber | varchar(50) | 50 | NULL allowed |  |
| calledNumber_wnpID | int | 4 | NULL allowed |  |
| calledNumber_CC | varchar(10) | 10 | NULL allowed |  |
| calledNumber_NDC | varchar(10) | 10 | NULL allowed |  |
| calledNumber_OrigDest | varchar(10) | 10 | NULL allowed |  |
| localTimeStamp | datetime | 8 | NULL allowed |  |
| utcTimeOffset | varchar(16) | 16 | NULL allowed |  |
| totalCallEventDuration | int | 4 | NULL allowed |  |
| recEntityCode | varchar(50) | 50 | NULL allowed |  |
| callReference | varchar(50) | 50 | NULL allowed |  |
| locationArea | varchar(20) | 20 | NULL allowed |  |
| cellId | int | 4 | NULL allowed |  |
| servingBid | varchar(50) | 50 | NULL allowed |  |
| servingLocationDescription | varchar(50) | 50 | NULL allowed |  |
| teleServiceCode | varchar(2) | 2 | NULL allowed |  |
| chargedItem | varchar(2) | 2 | NULL allowed |  |
| chargeType | varchar(2) | 2 | NULL allowed |  |
| charge | decimal(18,6) | 9 | NULL allowed |  |
| chargeableUnits | int | 4 | NULL allowed |  |
| chargedUnits | int | 4 | NULL allowed |  |
| calledPlace | varchar(20) | 20 | NULL allowed |  |
| calledRegion | varchar(20) | 20 | NULL allowed |  |
| imei | varchar(12) | 12 | NULL allowed |  |
| taxCode | int | 4 | NULL allowed |  |
| taxValue | decimal(18,6) | 9 | NULL allowed |  |
| CAMELServiceLevel | varchar(16) | 16 | NULL allowed |  |
| CAMELServiceKey | int | 4 | NULL allowed |  |
| CAMELtaxCode | int | 4 | NULL allowed |  |
| CAMELtaxValue | decimal(18,6) | 9 | NULL allowed |  |
| CAMELInvocationFee | decimal(18,6) | 9 | NULL allowed |  |
| CAMELexchangeRateCode | int | 4 | NULL allowed |  |
| CAMEL3GDestinationNumber | varchar(32) | 32 | NULL allowed |  |
| CAMELSEInformation | varchar(256) | 256 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

