#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.Inbound_GPRS

# ![Tables](../../../../Images/Table32.png) [dbo].[Inbound_GPRS]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_Inbound_GPRS: BatchID\ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_ExporterMoveToWorkItems
IX_IDAgreementUsedToRate
IX_IDOperator
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IdOperatorWfStateDate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(6) | BatchID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_DMP_Inbound_GPRS: BatchID\ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_ExporterMoveToWorkItems
IX_IDAgreementUsedToRate
IX_IDOperator
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IdOperatorWfStateDate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(6) | ID | int | 4 | NOT NULL |
| [![Indexes IX_IdOperatorWfStateDate](../../../../Images/Index.png)](#indexes) | WF_STATE | int | 4 | NOT NULL |
| [![Indexes IX_IDAgreementUsedToRate
IX_IDOperator
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IdOperatorWfStateDate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(5) | IDOperator | bigint | 8 | NULL allowed |
| [![Indexes IX_IDAgreementUsedToRate
IX_IDOperator
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(4) | IDAgreement | bigint | 8 | NULL allowed |
| [![Indexes IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | MSISDN | varchar(32) | 32 | NULL allowed |
|  | MSISDN_WNP | int | 4 | NULL allowed |
| [![Indexes IX_IDOperator](../../../../Images/Index.png)](#indexes) | MSISDN_CC | varchar(7) | 7 | NULL allowed |
|  | MSISDN_NDC | varchar(7) | 7 | NULL allowed |
|  | MSISDN_OrigDest | varchar(7) | 7 | NULL allowed |
|  | MSISDN_TON | tinyint | 1 | NULL allowed |
|  | MSISDN_NPI | tinyint | 1 | NULL allowed |
| [![Indexes IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | IMSI | varchar(32) | 32 | NULL allowed |
| [![Indexes IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | IMEI | varchar(32) | 32 | NULL allowed |
| [![Indexes IX_IDAgreementUsedToRate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | ZoneID | varchar(7) | 7 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | pdpAddress | varchar(45) | 45 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | ggsnAddress | varchar(45) | 45 | NULL allowed |
|  | sgsnAddress | varchar(45) | 45 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | AccessPointNameNI | varchar(65) | 65 | NULL allowed |
| [![Indexes IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | AccessPointNameOI | varchar(65) | 65 | NULL allowed |
| [![Indexes IX_IDAgreementUsedToRate
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(3) | chargingID | bigint | 8 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | DataVolumeIncoming | bigint | 8 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | DataVolumeOutgoing | bigint | 8 | NULL allowed |
| [![Indexes IX_DATE_BEGIN_CALL
IX_IDAgreementUsedToRate
IX_IDOperator
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IdOperatorWfStateDate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(6) | Date_Begin_Call | datetime | 8 | NULL allowed |
| [![Indexes IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | Date_End_Call | datetime | 8 | NULL allowed |
| [![Indexes IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | CallDuration | int | 4 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | CauseForTerm | int | 4 | NULL allowed |
|  | recordSequenceNumber | int | 4 | NULL allowed |
|  | nodeID | varchar(21) | 21 | NULL allowed |
|  | localSequenceNumber | int | 4 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | lac | int | 4 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | cellID | int | 4 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | Begin_Day_Type | varchar(2) | 2 | NULL allowed |
|  | End_Day_Type | varchar(2) | 2 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | Initial_Schedule_Type | int | 4 | NOT NULL |
|  | Final_Schedule_Type | int | 4 | NOT NULL |
| [![Indexes IX_IDAgreementUsedToRate
IX_IDOperator
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(3) | RateValue | numeric(18,10) | 9 | NOT NULL |
| [![Indexes IX_IDOperator](../../../../Images/Index.png)](#indexes) | RoamingRateValue | numeric(18,10) | 9 | NOT NULL |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | chargedItem | varchar(2) | 2 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | chargeType | varchar(2) | 2 | NULL allowed |
| [![Indexes IX_IDAgreementUsedToRate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | chargeableUnits | bigint | 8 | NULL allowed |
| [![Indexes IX_IDAgreementUsedToRate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | chargedUnits | bigint | 8 | NULL allowed |
| [![Indexes IX_ExporterMoveToWorkItems
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(2) | TAPRoaming_State | int | 4 | NOT NULL |
| [![Indexes IX_IDAgreementUsedToRate
ix_Inbound_GPRS_IDOperator_IDAgreement_ChargingID_IDAgreementUsedToRate
IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes)(3) | IDAgreementUsedToRate | bigint | 8 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | isCAMELCall | bit | 1 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | CAMELServiceLevel | varchar(13) | 13 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | CAMELServiceKey | int | 4 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | defaultCallHandling | smallint | 2 | NULL allowed |
| [![Indexes IX_IMSI_TAPRoamingState](../../../../Images/Index.png)](#indexes) | CamelExtraInformation | varchar(max) | max | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

