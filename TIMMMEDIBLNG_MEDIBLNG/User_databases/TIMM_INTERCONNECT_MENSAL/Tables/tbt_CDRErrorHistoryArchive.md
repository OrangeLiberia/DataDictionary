#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.tbt_CDRErrorHistoryArchive

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_CDRErrorHistoryArchive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_CDRErrorHistoryArchive: FK_FileDesc_ID\FileID\CDRID\ErrorID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | FK_FileDesc_ID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_tbt_CDRErrorHistoryArchive: FK_FileDesc_ID\FileID\CDRID\ErrorID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_tbt_CDRErrorHistoryArchive: FK_FileDesc_ID\FileID\CDRID\ErrorID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_tbt_CDRErrorHistoryArchive: FK_FileDesc_ID\FileID\CDRID\ErrorID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | ErrorID | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_tbt_CDRErrorHistoryArchive: FK_FileDesc_ID\FileID\CDRID\ErrorID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | FK_Central_ID | int | 4 | NOT NULL |  |
|  | Reprocessed | int | 4 | NOT NULL | ((0)) |
|  | LinkedID | int | 4 | NULL allowed |  |
|  | CllgnNumber | varchar(32) | 32 | NULL allowed |  |
|  | FK_WNP_ID_CllgnNumber | int | 4 | NULL allowed |  |
|  | DialedNumber | varchar(32) | 32 | NULL allowed |  |
|  | FK_WNP_ID_DialedNumber | int | 4 | NULL allowed |  |
|  | CalledNumber | varchar(32) | 32 | NULL allowed |  |
|  | FK_WNP_ID_CalledNumber | int | 4 | NULL allowed |  |
|  | OrigTime | datetime | 8 | NULL allowed |  |
|  | DiscTime | datetime | 8 | NULL allowed |  |
|  | CallDuration | int | 4 | NULL allowed |  |
|  | AnswerType | tinyint | 1 | NULL allowed |  |
|  | ReleaseCallType | tinyint | 1 | NULL allowed |  |
|  | Trunk_IN | int | 4 | NULL allowed |  |
|  | Trunk_Out | int | 4 | NULL allowed |  |
|  | lastdateupdated | datetime | 8 | NULL allowed |  |
|  | lastuserupdated | int | 4 | NULL allowed |  |
|  | Num_Chamadas | int | 4 | NULL allowed | ((1)) |
|  | ReverseCDR | int | 4 | NULL allowed | ((0)) |
|  | FK_WNP_ID_CllgnNumber_Original | int | 4 | NULL allowed |  |
|  | lastdateArchived | datetime | 8 | NULL allowed |  |
|  | lastuserArchived | int | 4 | NULL allowed |  |
|  | SMS_Length | int | 4 | NULL allowed |  |
|  | Tipo_Servico_ID | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

