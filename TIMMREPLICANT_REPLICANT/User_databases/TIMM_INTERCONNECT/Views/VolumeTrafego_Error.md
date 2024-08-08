#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Views](Views.md) > dbo.VolumeTrafego_Error

# ![Views](../../../../Images/View32.png) [dbo].[VolumeTrafego_Error]

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
| ErrorID | int | 4 |
| FK_Central_ID | int | 4 |
| Reprocessed | int | 4 |
| LinkedID | int | 4 |
| CllgnNumber | varchar(32) | 32 |
| CNS_Origem_ID | int | 4 |
| CNS_Destino_ID | int | 4 |
| FK_WNP_ID_DialedNumber | int | 4 |
| CalledNumber | varchar(32) | 32 |
| FK_WNP_ID_CalledNumber | int | 4 |
| Data_Registo | datetime | 8 |
| Data_Registo_Fim | datetime | 8 |
| Volume_Trafego_Segundos | int | 4 |
| AnswerType | tinyint | 1 |
| ReleaseCallType | tinyint | 1 |
| Trunk_IN | int | 4 |
| Trunk_Out | int | 4 |
| Data_Calculo | datetime | 8 |
| lastuserupdated | int | 4 |
| Num_Chamadas | int | 4 |
| ReverseCDR | int | 4 |
| IsHubbing | int | 4 |
| FK_Moeda_ID | int | 4 |
| Acordo_ID | int | 4 |
| Hubbing_ID | int | 4 |
| tipo_trafego_id | int | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

