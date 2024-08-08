#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.Inbound_GPRS_History_2014

# ![Tables](../../../../Images/Table32.png) [dbo].[Inbound_GPRS_History_2014]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_Inbound_GPRS_History_2014: BatchID\ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_ExporterMoveToWorkItems](../../../../Images/Index.png)](#indexes) | BatchID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_DMP_Inbound_GPRS_History_2014: BatchID\ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_ExporterMoveToWorkItems](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | WF_STATE | int | 4 | NOT NULL |
|  | IDOperator | bigint | 8 | NULL allowed |
|  | IDAgreement | bigint | 8 | NULL allowed |
|  | MSISDN | varchar(32) | 32 | NULL allowed |
|  | MSISDN_WNP | int | 4 | NULL allowed |
|  | MSISDN_CC | varchar(7) | 7 | NULL allowed |
|  | MSISDN_NDC | varchar(7) | 7 | NULL allowed |
|  | MSISDN_OrigDest | varchar(7) | 7 | NULL allowed |
|  | MSISDN_TON | tinyint | 1 | NULL allowed |
|  | MSISDN_NPI | tinyint | 1 | NULL allowed |
|  | IMSI | varchar(32) | 32 | NULL allowed |
|  | IMEI | varchar(32) | 32 | NULL allowed |
|  | ZoneID | varchar(7) | 7 | NULL allowed |
|  | pdpAddress | varchar(45) | 45 | NULL allowed |
|  | ggsnAddress | varchar(45) | 45 | NULL allowed |
|  | sgsnAddress | varchar(45) | 45 | NULL allowed |
|  | AccessPointNameNI | varchar(65) | 65 | NULL allowed |
|  | AccessPointNameOI | varchar(65) | 65 | NULL allowed |
|  | chargingID | bigint | 8 | NULL allowed |
|  | DataVolumeIncoming | bigint | 8 | NULL allowed |
|  | DataVolumeOutgoing | bigint | 8 | NULL allowed |
| [![Indexes IX_DATE_BEGIN_CALL](../../../../Images/Index.png)](#indexes) | Date_Begin_Call | datetime | 8 | NULL allowed |
|  | Date_End_Call | datetime | 8 | NULL allowed |
|  | CallDuration | int | 4 | NULL allowed |
|  | CauseForTerm | int | 4 | NULL allowed |
|  | recordSequenceNumber | int | 4 | NULL allowed |
|  | nodeID | varchar(21) | 21 | NULL allowed |
|  | localSequenceNumber | int | 4 | NULL allowed |
|  | lac | int | 4 | NULL allowed |
|  | cellID | int | 4 | NULL allowed |
|  | Begin_Day_Type | varchar(2) | 2 | NULL allowed |
|  | End_Day_Type | varchar(2) | 2 | NULL allowed |
|  | Initial_Schedule_Type | int | 4 | NOT NULL |
|  | Final_Schedule_Type | int | 4 | NOT NULL |
|  | RateValue | numeric(18,10) | 9 | NOT NULL |
|  | RoamingRateValue | numeric(18,10) | 9 | NOT NULL |
|  | chargedItem | varchar(2) | 2 | NULL allowed |
|  | chargeType | varchar(2) | 2 | NULL allowed |
|  | chargeableUnits | bigint | 8 | NULL allowed |
|  | chargedUnits | bigint | 8 | NULL allowed |
| [![Indexes IX_ExporterMoveToWorkItems](../../../../Images/Index.png)](#indexes) | TAPRoaming_State | int | 4 | NOT NULL |
|  | IDAgreementUsedToRate | bigint | 8 | NULL allowed |
|  | isCAMELCall | bit | 1 | NULL allowed |
|  | CAMELServiceLevel | varchar(13) | 13 | NULL allowed |
|  | CAMELServiceKey | int | 4 | NULL allowed |
|  | defaultCallHandling | smallint | 2 | NULL allowed |
|  | CamelExtraInformation | varchar(max) | max | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

