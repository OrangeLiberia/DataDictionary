#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Views](Views.md) > dbo.VolumeDados

# ![Views](../../../../Images/View32.png) [dbo].[VolumeDados]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| FK_FileDesc_ID | bigint | 8 |
| FileID | bigint | 8 |
| CDRID | int | 4 |
| p_status | int | 4 |
| LinkedID | int | 4 |
| ErrorID | int | 4 |
| FK_Central_ID | int | 4 |
| CllgnNumber | varchar(32) | 32 |
| CNS_Origem_ID | int | 4 |
| DialedNumber | varchar(32) | 32 |
| FK_WNP_ID_DialedNumber | int | 4 |
| CalledNumber | varchar(32) | 32 |
| CNS_Destino_ID | int | 4 |
| Data_Registo | datetime | 8 |
| Data_Registo_Fim | datetime | 8 |
| Volume_Trafego_Segundos | int | 4 |
| AnswerType | tinyint | 1 |
| ReleaseCallType | tinyint | 1 |
| Trunk_IN | int | 4 |
| Trunk_Out | int | 4 |
| ReverseCDR | int | 4 |
| FK_WNP_ID_CllgnNumber_Original | int | 4 |
| Minute_rate | numeric(18,6) | 9 |
| Imposto | numeric(18,6) | 9 |
| Acordo_ID | int | 4 |
| Hubbing_ID | int | 4 |
| TipoRate_id | int | 4 |
| Tipo_Servico_ID | int | 4 |
| ID_OrigemTrafego | int | 4 |
| TipoOTTrafego_id | int | 4 |
| tipo_trafego_id | int | 4 |
| FK_Moeda_ID | int | 4 |
| num_chamadas | int | 4 |
| Parent_ID | int | 4 |
| Tipo_Horario | varchar(max) | max |
| Volume_Trafego_Moeda | numeric(18,6) | 9 |
| Data_Calculo | datetime | 8 |
| Status | int | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

