#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_Repository_ImportedCDRs

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_Repository_ImportedCDRs]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
|  | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes FileDescriptorID
IX_localTimeStamp](../../../../Images/Index.png)](#indexes)(2) | FileDescriptorID | bigint | 8 | NOT NULL |  |
| [![Indexes IX_localTimeStamp
RoamingType](../../../../Images/Index.png)](#indexes)(2) | RoamingType | varchar(10) | 10 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | imsi | varchar(15) | 15 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | msisdn | varchar(50) | 50 | NULL allowed |  |
|  | msisdn_wnpID | int | 4 | NULL allowed |  |
|  | msisdn_CC | varchar(10) | 10 | NULL allowed |  |
|  | msisdn_NDC | varchar(10) | 10 | NULL allowed |  |
|  | msisdn_OrigDest | varchar(10) | 10 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | calledNumber | varchar(50) | 50 | NULL allowed |  |
|  | calledNumber_wnpID | int | 4 | NULL allowed |  |
|  | calledNumber_CC | varchar(10) | 10 | NULL allowed |  |
|  | calledNumber_NDC | varchar(10) | 10 | NULL allowed |  |
|  | calledNumber_OrigDest | varchar(10) | 10 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | localTimeStamp | datetime | 8 | NULL allowed |  |
|  | utcTimeOffset | varchar(16) | 16 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | totalCallEventDuration | int | 4 | NULL allowed |  |
|  | recEntityCode | varchar(50) | 50 | NULL allowed |  |
|  | callReference | varchar(50) | 50 | NULL allowed |  |
|  | locationArea | varchar(20) | 20 | NULL allowed |  |
|  | cellId | int | 4 | NULL allowed |  |
|  | servingBid | varchar(50) | 50 | NULL allowed |  |
|  | servingLocationDescription | varchar(50) | 50 | NULL allowed |  |
|  | teleServiceCode | varchar(2) | 2 | NULL allowed |  |
|  | chargedItem | varchar(2) | 2 | NULL allowed |  |
|  | chargeType | varchar(2) | 2 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | charge | decimal(18,6) | 9 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | chargeableUnits | int | 4 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | chargedUnits | int | 4 | NULL allowed |  |
|  | calledPlace | varchar(20) | 20 | NULL allowed |  |
|  | calledRegion | varchar(20) | 20 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | imei | varchar(12) | 12 | NULL allowed |  |
|  | taxCode | int | 4 | NULL allowed |  |
| [![Indexes IX_localTimeStamp](../../../../Images/Index.png)](#indexes) | taxValue | decimal(18,6) | 9 | NULL allowed |  |
|  | CAMELServiceLevel | varchar(16) | 16 | NULL allowed |  |
|  | CAMELServiceKey | int | 4 | NULL allowed |  |
|  | CAMELtaxCode | int | 4 | NULL allowed |  |
|  | CAMELtaxValue | decimal(18,6) | 9 | NULL allowed |  |
|  | CAMELInvocationFee | decimal(18,6) | 9 | NULL allowed |  |
|  | CAMELexchangeRateCode | int | 4 | NULL allowed |  |
|  | CAMEL3GDestinationNumber | varchar(32) | 32 | NULL allowed |  |
|  | CAMELSEInformation | varchar(256) | 256 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

