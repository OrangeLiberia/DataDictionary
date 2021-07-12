#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.CDRDadosInterconnect

# ![Tables](../../../../Images/Table32.png) [dbo].[CDRDadosInterconnect]

---

## <a name="#description"></a>MS_Description

Original Imported CDRs

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CDRDadosInterconnect: FK_FileDesc_ID\FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FK_FileDesc_ID | bigint | 8 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CDRDadosInterconnect: FK_FileDesc_ID\FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  | _Batch ID_ |
| [![Cluster Primary Key PK_CDRDadosInterconnect: FK_FileDesc_ID\FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |  |  |
|  | LinkedID | int | 4 | NULL allowed |  |  |
|  | CllgnNumber | varchar(32) | 32 | NULL allowed |  |  |
|  | FK_WNP_ID_CllgnNumber | int | 4 | NULL allowed |  | _World Numbering Plan_ |
|  | DialedNumber | varchar(32) | 32 | NULL allowed |  |  |
|  | FK_WNP_ID_DialedNumber | int | 4 | NULL allowed |  |  |
|  | CalledNumber | varchar(32) | 32 | NULL allowed |  |  |
|  | FK_WNP_ID_CalledNumber | int | 4 | NULL allowed | ((0)) |  |
|  | OrigTime | datetime | 8 | NULL allowed |  |  |
|  | DiscTime | datetime | 8 | NULL allowed |  |  |
|  | CallDuration | int | 4 | NULL allowed |  | _Duração da Chamada <> DiscTime-OrigTime (Ocupação de Rede)_ |
|  | AnswerType | tinyint | 1 | NULL allowed |  |  |
|  | ReleaseCallType | tinyint | 1 | NULL allowed |  |  |
|  | Trunk_IN | int | 4 | NULL allowed |  |  |
|  | Trunk_Out | int | 4 | NULL allowed |  |  |
|  | FK_WNP_ID_CllgnNumber_Original | int | 4 | NULL allowed |  |  |
|  | ReverseCDR | int | 4 | NULL allowed | ((0)) |  |
|  | VTrunk_IN | varchar(50) | 50 | NULL allowed |  |  |
|  | VTrunk_OUT | varchar(50) | 50 | NULL allowed |  |  |
|  | SMS_Length | int | 4 | NULL allowed |  |  |
|  | Tipo_Servico_ID | int | 4 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

