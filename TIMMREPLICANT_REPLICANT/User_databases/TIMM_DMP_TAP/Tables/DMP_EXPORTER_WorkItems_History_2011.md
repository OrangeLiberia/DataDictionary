#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_EXPORTER_WorkItems_History_2011

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_EXPORTER_WorkItems_History_2011]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_EXPORTER_WorkItems_History_2011: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL |
|  | SpecificDay | datetime | 8 | NOT NULL |
|  | FilePrefix | varchar(2) | 2 | NOT NULL |
|  | Sender | varchar(5) | 5 | NOT NULL |
|  | Recipient | varchar(5) | 5 | NOT NULL |
|  | Sequence | varchar(5) | 5 | NOT NULL |
|  | TipoAcordo | varchar(1) | 1 | NOT NULL |
|  | recEntityCode_A | int | 4 | NULL allowed |
|  | recEntityType_A | int | 4 | NULL allowed |
|  | recEntityId_A | varchar(45) | 45 | NULL allowed |
|  | recEntityCode_B | int | 4 | NULL allowed |
|  | recEntityType_B | int | 4 | NULL allowed |
|  | recEntityId_B | varchar(45) | 45 | NULL allowed |
|  | batchid | bigint | 8 | NULL allowed |
|  | CDRID | int | 4 | NULL allowed |
|  | RoamingType | int | 4 | NULL allowed |
|  | imsi | varchar(32) | 32 | NULL allowed |
|  | imei | varchar(32) | 32 | NULL allowed |
|  | callingNumber | varchar(32) | 32 | NULL allowed |
|  | calledNumber | varchar(32) | 32 | NULL allowed |
|  | dialledDigits | varchar(32) | 32 | NULL allowed |
|  | msisdn | varchar(32) | 32 | NULL allowed |
|  | localTimeStamp | datetime | 8 | NULL allowed |
|  | totalCallEventDuration | int | 4 | NULL allowed |
|  | locationArea | int | 4 | NULL allowed |
|  | cellId | int | 4 | NULL allowed |
|  | teleServiceCode | varchar(2) | 2 | NULL allowed |
|  | chargedItem | varchar(2) | 2 | NULL allowed |
|  | callTypeLevel1 | int | 4 | NULL allowed |
|  | calledCountryCode | varchar(256) | 256 | NULL allowed |
|  | chargeType | varchar(2) | 2 | NULL allowed |
|  | charge | numeric(18,10) | 9 | NULL allowed |
|  | chargeableUnits | int | 4 | NULL allowed |
|  | chargedUnits | int | 4 | NULL allowed |
|  | calledPlace | varchar(256) | 256 | NULL allowed |
|  | calledRegion | varchar(256) | 256 | NULL allowed |
|  | taxCode_Taxation | int | 4 | NULL allowed |
|  | taxType_Taxation | varchar(2) | 2 | NULL allowed |
|  | taxRate_Taxation | varchar(10) | 10 | NULL allowed |
|  | taxCode | int | 4 | NULL allowed |
|  | taxValue | numeric(18,10) | 9 | NULL allowed |
|  | dayCategory | varchar(50) | 50 | NULL allowed |
|  | timeBand | varchar(50) | 50 | NULL allowed |
|  | supplServiceCode | varchar(2) | 2 | NULL allowed |
|  | supplServiceActionCode | int | 4 | NULL allowed |
|  | thirdPartyNumber | varchar(32) | 32 | NULL allowed |
|  | clirIndicator | tinyint | 1 | NULL allowed |
|  | PdpAddress | varchar(45) | 45 | NULL allowed |
|  | AccessPointNameNI | varchar(65) | 65 | NULL allowed |
|  | AccessPointNameOI | varchar(65) | 65 | NULL allowed |
|  | CauseForTerm | varchar(20) | 20 | NULL allowed |
|  | chargingID | bigint | 8 | NULL allowed |
|  | DataVolumeIncoming | bigint | 8 | NULL allowed |
|  | DataVolumeOutgoing | bigint | 8 | NULL allowed |
|  | ExecState | smallint | 2 | NOT NULL |
|  | InstanceName | varchar(50) | 50 | NULL allowed |
|  | InstanceNameExec | varchar(50) | 50 | NULL allowed |
|  | ReExecutions | int | 4 | NOT NULL |
|  | Comment | varchar(50) | 50 | NULL allowed |
|  | InsertDate | datetime | 8 | NOT NULL |
|  | SelectDate | datetime | 8 | NULL allowed |
|  | LastUpdate | datetime | 8 | NULL allowed |
|  | LastExecDate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | FileDescriptorID | bigint | 8 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

