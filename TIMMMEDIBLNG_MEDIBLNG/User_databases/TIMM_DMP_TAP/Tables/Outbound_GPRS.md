#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.Outbound_GPRS

# ![Tables](../../../../Images/Table32.png) [dbo].[Outbound_GPRS]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
|  | WF_STATE | int | 4 | NULL allowed |
| [![Cluster Primary Key PK_Outbound_GPRS: FileDescriptorID\CDRid](../../../../Images/pkcluster.png)](#indexes) | FileDescriptorID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_Outbound_GPRS: FileDescriptorID\CDRid](../../../../Images/pkcluster.png)](#indexes) | CDRid | int | 4 | NOT NULL |
|  | msisdn | varchar(32) | 32 | NULL allowed |
|  | msisdn_wnpID | int | 4 | NULL allowed |
|  | msisdn_CC | varchar(7) | 7 | NULL allowed |
|  | msisdn_NDC | varchar(7) | 7 | NULL allowed |
|  | msisdn_OrigDest | varchar(7) | 7 | NULL allowed |
|  | msisdn_TON | tinyint | 1 | NULL allowed |
|  | msisdn_NPI | tinyint | 1 | NULL allowed |
|  | imsi | varchar(32) | 32 | NULL allowed |
|  | imei | varchar(32) | 32 | NULL allowed |
|  | pdpAddress | varchar(45) | 45 | NULL allowed |
|  | ggsnAddress | varchar(45) | 45 | NULL allowed |
|  | sgsnAddress | varchar(45) | 45 | NULL allowed |
|  | accessPointNameNI | varchar(65) | 65 | NULL allowed |
|  | accessPointNameOI | varchar(65) | 65 | NULL allowed |
|  | dataVolumeIncoming | bigint | 8 | NULL allowed |
|  | dataVolumeOutgoing | bigint | 8 | NULL allowed |
|  | localTimeStamp | datetime | 8 | NULL allowed |
|  | utcTimeOffsetCode | varchar(16) | 16 | NULL allowed |
|  | CallDuration | int | 4 | NULL allowed |
|  | causeForTerm | int | 4 | NULL allowed |
|  | chargingID | bigint | 8 | NULL allowed |
|  | RecEntityCode | int | 4 | NULL allowed |
|  | lac | int | 4 | NULL allowed |
|  | cellID | int | 4 | NULL allowed |
|  | servingLocationDescription | varchar(50) | 50 | NULL allowed |
|  | OperatorSpecInformation | varchar(50) | 50 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

