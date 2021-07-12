#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vwt_DMP_EXPORTER_WorkItems_History_All

# ![Views](../../../../Images/View32.png) [dbo].[vwt_DMP_EXPORTER_WorkItems_History_All]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | bigint | 8 |
| SpecificDay | datetime | 8 |
| FilePrefix | varchar(2) | 2 |
| Sender | varchar(5) | 5 |
| Recipient | varchar(5) | 5 |
| Sequence | varchar(5) | 5 |
| TipoAcordo | varchar(1) | 1 |
| recEntityCode_A | int | 4 |
| recEntityType_A | int | 4 |
| recEntityId_A | varchar(45) | 45 |
| recEntityCode_B | int | 4 |
| recEntityType_B | int | 4 |
| recEntityId_B | varchar(45) | 45 |
| batchid | bigint | 8 |
| CDRID | int | 4 |
| RoamingType | int | 4 |
| imsi | varchar(32) | 32 |
| imei | varchar(32) | 32 |
| callingNumber | varchar(32) | 32 |
| calledNumber | varchar(32) | 32 |
| dialledDigits | varchar(32) | 32 |
| msisdn | varchar(32) | 32 |
| localTimeStamp | datetime | 8 |
| totalCallEventDuration | int | 4 |
| locationArea | int | 4 |
| cellId | int | 4 |
| teleServiceCode | varchar(2) | 2 |
| chargedItem | varchar(2) | 2 |
| callTypeLevel1 | int | 4 |
| calledCountryCode | varchar(256) | 256 |
| chargeType | varchar(2) | 2 |
| charge | numeric(18,10) | 9 |
| chargeableUnits | bigint | 8 |
| chargedUnits | bigint | 8 |
| calledPlace | varchar(256) | 256 |
| calledRegion | varchar(256) | 256 |
| taxCode_Taxation | int | 4 |
| taxType_Taxation | varchar(2) | 2 |
| taxRate_Taxation | varchar(10) | 10 |
| taxCode | int | 4 |
| taxValue | numeric(18,10) | 9 |
| dayCategory | varchar(50) | 50 |
| timeBand | varchar(50) | 50 |
| supplServiceCode | varchar(2) | 2 |
| supplServiceActionCode | int | 4 |
| thirdPartyNumber | varchar(32) | 32 |
| clirIndicator | tinyint | 1 |
| PdpAddress | varchar(45) | 45 |
| AccessPointNameNI | varchar(65) | 65 |
| AccessPointNameOI | varchar(65) | 65 |
| CauseForTerm | varchar(20) | 20 |
| chargingID | bigint | 8 |
| DataVolumeIncoming | bigint | 8 |
| DataVolumeOutgoing | bigint | 8 |
| ExecState | smallint | 2 |
| InstanceName | varchar(50) | 50 |
| InstanceNameExec | varchar(50) | 50 |
| ReExecutions | int | 4 |
| Comment | varchar(50) | 50 |
| InsertDate | datetime | 8 |
| SelectDate | datetime | 8 |
| LastUpdate | datetime | 8 |
| LastExecDate | datetime | 8 |
| LastUserID | int | 4 |
| FileDescriptorID | bigint | 8 |
| isCAMELCall | bit | 1 |
| CAMELServiceLevel | varchar(13) | 13 |
| CAMELServiceKey | int | 4 |
| defaultCallHandling | smallint | 2 |
| CamelExtraInformation | varchar(max) | max |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

