#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_IMPORTER_NRTRDE_MTC

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_IMPORTER_NRTRDE_MTC]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_MTC: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_MTC: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
|  | RecordType | varchar(20) | 20 | NULL allowed |
|  | IMSI | varchar(20) | 20 | NULL allowed |
|  | IMEI | varchar(20) | 20 | NULL allowed |
|  | CallEventStart | varchar(20) | 20 | NULL allowed |
|  | UTCTimeOffset | varchar(50) | 50 | NULL allowed |
|  | CallEventDuration | int | 4 | NULL allowed |
|  | TerminationCause | varchar(2) | 2 | NULL allowed |
|  | BearerServiceCode | varchar(2) | 2 | NULL allowed |
|  | TeleServiceCode | varchar(2) | 2 | NULL allowed |
|  | CallingNumber | varchar(20) | 20 | NULL allowed |
|  | RecordEntityID | varchar(32) | 32 | NULL allowed |
|  | CallReference | varchar(20) | 20 | NULL allowed |
|  | UNKNOWN | varchar(max) | max | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

