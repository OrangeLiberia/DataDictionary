#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.IconExtract

# ![Tables](../../../../Images/Table32.png) [dbo].[IconExtract]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| FK_FileDesc_ID | bigint | 8 | NOT NULL |
| FileID | bigint | 8 | NOT NULL |
| CDRID | int | 4 | NOT NULL |
| p_status | int | 4 | NULL allowed |
| LinkedID | int | 4 | NULL allowed |
| ErrorID | int | 4 | NULL allowed |
| FK_Central_ID | int | 4 | NOT NULL |
| CllgnNumber | varchar(32) | 32 | NULL allowed |
| FK_WNP_ID_CllgnNumber | int | 4 | NULL allowed |
| DialedNumber | varchar(32) | 32 | NULL allowed |
| FK_WNP_ID_DialedNumber | int | 4 | NULL allowed |
| CalledNumber | varchar(32) | 32 | NULL allowed |
| FK_WNP_ID_CalledNumber | int | 4 | NULL allowed |
| OrigTime | datetime | 8 | NULL allowed |
| DiscTime | datetime | 8 | NULL allowed |
| CallDuration | int | 4 | NULL allowed |
| AnswerType | tinyint | 1 | NULL allowed |
| ReleaseCallType | tinyint | 1 | NULL allowed |
| Trunk_IN | int | 4 | NULL allowed |
| Trunk_Out | int | 4 | NULL allowed |
| ReverseCDR | int | 4 | NULL allowed |
| FK_WNP_ID_CllgnNumber_Original | int | 4 | NULL allowed |
| Minute_rate | float | 8 | NULL allowed |
| Imposto | float | 8 | NULL allowed |
| IDAgreement | int | 4 | NULL allowed |
| IDHubbing | int | 4 | NULL allowed |
| TipoRate_id | int | 4 | NULL allowed |
| Tipo_Servico_ID | int | 4 | NULL allowed |
| ID_OrigemTrafego | int | 4 | NULL allowed |
| ID_DestinoTrafego | int | 4 | NULL allowed |
| tipo_trafego_id | int | 4 | NOT NULL |
| FK_Moeda_ID | int | 4 | NULL allowed |
| num_Chamada | int | 4 | NOT NULL |
| Parent_ID | int | 4 | NULL allowed |
| Tipo_Horario | varchar(max) | max | NULL allowed |
| Volume_Trafego_Moeda | float | 8 | NULL allowed |
| Data_Calculo | datetime | 8 | NULL allowed |
| Status | int | 4 | NOT NULL |
| FinalStatus | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

