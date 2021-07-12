#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.tbt_VolumeTrafego

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_VolumeTrafego]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_VolumeTrafego: FK_FileDesc_ID\FileID\CDRID\tipo_trafego_id\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_PROCESS
IX_IDDestTrafego
IX_Trafego_Servico_OrigTime
IX_ProcessUpdatePriceCount](../../../../Images/Index.png)](#indexes)(4) | FK_FileDesc_ID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_tbt_VolumeTrafego: FK_FileDesc_ID\FileID\CDRID\tipo_trafego_id\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_PROCESS
IX_IDDestTrafego
IX_Trafego_Servico_OrigTime
IX_ProcessUpdatePriceCount](../../../../Images/Index.png)](#indexes)(4) | FileID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_tbt_VolumeTrafego: FK_FileDesc_ID\FileID\CDRID\tipo_trafego_id\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_PROCESS
IX_IDDestTrafego
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(3) | CDRID | int | 4 | NOT NULL |  |
|  | p_status | int | 4 | NULL allowed |  |
|  | LinkedID | int | 4 | NULL allowed |  |
|  | ErrorID | int | 4 | NULL allowed |  |
| [![Cluster Primary Key PK_tbt_VolumeTrafego: FK_FileDesc_ID\FileID\CDRID\tipo_trafego_id\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_PROCESS
IX_IDDestTrafego
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(3) | FK_Central_ID | int | 4 | NOT NULL |  |
| [![Indexes IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(2) | CllgnNumber | varchar(32) | 32 | NULL allowed |  |
| [![Indexes IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(2) | FK_WNP_ID_CllgnNumber | int | 4 | NULL allowed |  |
|  | DialedNumber | varchar(32) | 32 | NULL allowed |  |
|  | FK_WNP_ID_DialedNumber | int | 4 | NULL allowed |  |
| [![Indexes IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(2) | CalledNumber | varchar(32) | 32 | NULL allowed |  |
| [![Indexes IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(2) | FK_WNP_ID_CalledNumber | int | 4 | NULL allowed |  |
| [![Indexes IX_PROCESS
IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(3) | OrigTime | datetime | 8 | NULL allowed |  |
|  | DiscTime | datetime | 8 | NULL allowed |  |
| [![Indexes IX_PROCESS
IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(3) | CallDuration | int | 4 | NULL allowed |  |
|  | AnswerType | tinyint | 1 | NULL allowed |  |
|  | ReleaseCallType | tinyint | 1 | NULL allowed |  |
|  | Trunk_IN | int | 4 | NULL allowed |  |
|  | Trunk_Out | int | 4 | NULL allowed |  |
|  | ReverseCDR | int | 4 | NULL allowed | ((0)) |
| [![Indexes IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(2) | FK_WNP_ID_CllgnNumber_Original | int | 4 | NULL allowed |  |
| [![Indexes IX_PROCESS](../../../../Images/Index.png)](#indexes) | Minute_rate | numeric(18,6) | 9 | NULL allowed |  |
|  | Imposto | numeric(18,6) | 9 | NULL allowed |  |
| [![Indexes IX_PROCESS
IX_ProcessUpdatePriceCount](../../../../Images/Index.png)](#indexes)(2) | IDAgreement | int | 4 | NULL allowed |  |
|  | IDHubbing | int | 4 | NULL allowed |  |
| [![Indexes IX_ProcessUpdatePriceCount](../../../../Images/Index.png)](#indexes) | TipoRate_id | int | 4 | NULL allowed |  |
| [![Indexes IX_PROCESS
IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(3) | Tipo_Servico_ID | int | 4 | NULL allowed |  |
| [![Indexes IX_PROCESS](../../../../Images/Index.png)](#indexes) | ID_OrigemTrafego | int | 4 | NULL allowed |  |
| [![Indexes IX_PROCESS
IX_IDDestTrafego](../../../../Images/Index.png)](#indexes)(2) | ID_DestinoTrafego | int | 4 | NULL allowed |  |
| [![Cluster Primary Key PK_tbt_VolumeTrafego: FK_FileDesc_ID\FileID\CDRID\tipo_trafego_id\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_PROCESS
IX_IDDestTrafego
IX_Calling_Called
IX_Trafego_Servico_OrigTime](../../../../Images/Index.png)](#indexes)(4) | tipo_trafego_id | int | 4 | NOT NULL | ((0)) |
|  | FK_Moeda_ID | int | 4 | NULL allowed |  |
|  | num_Chamada | int | 4 | NOT NULL | ((1)) |
|  | Parent_ID | int | 4 | NULL allowed |  |
|  | Tipo_Horario | varchar(max) | max | NULL allowed |  |
|  | Volume_Trafego_Moeda | numeric(18,6) | 9 | NULL allowed |  |
|  | Data_Calculo | datetime | 8 | NULL allowed |  |
|  | Status | int | 4 | NOT NULL | ((1)) |
|  | SMS_Length | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

