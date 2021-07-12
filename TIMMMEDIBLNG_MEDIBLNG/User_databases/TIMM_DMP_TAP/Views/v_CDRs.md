#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.v_CDRs

# ![Views](../../../../Images/View32.png) [dbo].[v_CDRs]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| AgreementID | bigint | 8 |
| IDOperator | bigint | 8 |
| recEntityCode_A | varchar(1) | 1 |
| recEntityType_A | varchar(1) | 1 |
| recEntityId_A | varchar(45) | 45 |
| recEntityCode_B | varchar(1) | 1 |
| recEntityType_B | varchar(1) | 1 |
| recEntityId_B | int | 4 |
| batchid | bigint | 8 |
| CDRID | int | 4 |
| RoamingType | int | 4 |
| imsi | varchar(32) | 32 |
| imei | varchar(32) | 32 |
| callingNumber | varchar(32) | 32 |
| calledNumber | varchar(32) | 32 |
| calledNumberCC | varchar(6) | 6 |
| dialledDigits | varchar(32) | 32 |
| msisdn | varchar(32) | 32 |
| localTimeStamp | datetime | 8 |
| totalCallEventDuration | varchar(30) | 30 |
| locationArea | int | 4 |
| cellID | int | 4 |
| supplServiceCode | varchar(2) | 2 |
| supplServiceActionCode | int | 4 |
| thirdPartyNumber | varchar(32) | 32 |
| clirIndicator | tinyint | 1 |
| teleServiceCode | varchar(2) | 2 |
| chargedItem | varchar(2) | 2 |
| callTypeLevel1 | int | 4 |
| calledCountryCode | varchar(256) | 256 |
| chargeType | varchar(2) | 2 |
| charge | numeric(23,10) | 13 |
| chargeableUnits | bigint | 8 |
| chargedUnits | bigint | 8 |
| TollTicketingInterval | int | 4 |
| TollTicketingRate | decimal(18,10) | 9 |
| BillingInterval | int | 4 |
| calledPlace | varchar(256) | 256 |
| calledRegion | varchar(256) | 256 |
| PdpAddress | varchar(45) | 45 |
| AccessPointNameNI | varchar(65) | 65 |
| AccessPointNameOI | varchar(65) | 65 |
| CauseForTerm | varchar(30) | 30 |
| chargingID | bigint | 8 |
| DataVolumeIncoming | bigint | 8 |
| DataVolumeOutgoing | bigint | 8 |
| TAPRoaming_State | int | 4 |
| isCAMELCall | bit | 1 |
| CAMELServiceLevel | varchar(13) | 13 |
| CAMELServiceKey | int | 4 |
| defaultCallHandling | smallint | 2 |
| CamelExtraInformation | varchar(max) | max |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

