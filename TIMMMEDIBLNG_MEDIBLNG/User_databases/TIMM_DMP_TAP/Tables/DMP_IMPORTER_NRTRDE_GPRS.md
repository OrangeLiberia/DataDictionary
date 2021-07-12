#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_IMPORTER_NRTRDE_GPRS

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_IMPORTER_NRTRDE_GPRS]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_GPRS: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_GPRS: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
|  | RecordType | varchar(20) | 20 | NULL allowed |
|  | IMSI | varchar(20) | 20 | NULL allowed |
|  | IMEI | varchar(20) | 20 | NULL allowed |
|  | CallEventStart | varchar(20) | 20 | NULL allowed |
|  | UTCTimeOffset | varchar(50) | 50 | NULL allowed |
|  | CallEventDuration | int | 4 | NULL allowed |
|  | TerminationCause | varchar(2) | 2 | NULL allowed |
|  | APNameNI | varchar(70) | 70 | NULL allowed |
|  | APNameOI | varchar(70) | 70 | NULL allowed |
|  | DataVolumeIn | int | 4 | NULL allowed |
|  | DataVolumeOut | int | 4 | NULL allowed |
|  | SGSNAddress | varchar(20) | 20 | NULL allowed |
|  | GGSNAddress | varchar(20) | 20 | NULL allowed |
|  | ChargingID | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

