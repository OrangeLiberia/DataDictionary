#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Views](Views.md) > dbo.tbt_CDRErrorTrunkOutNotDefined

# ![Views](../../../../Images/View32.png) [dbo].[tbt_CDRErrorTrunkOutNotDefined]

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
| FK_WNP_ID_CllgnNumber | int | 4 |
| DialedNumber | varchar(32) | 32 |
| FK_WNP_ID_DialedNumber | int | 4 |
| CalledNumber | varchar(32) | 32 |
| FK_WNP_ID_CalledNumber | int | 4 |
| OrigTime | datetime | 8 |
| DiscTime | datetime | 8 |
| CallDuration | int | 4 |
| AnswerType | tinyint | 1 |
| ReleaseCallType | tinyint | 1 |
| Trunk_IN | int | 4 |
| Trunk_Out | int | 4 |
| lastdateupdated | datetime | 8 |
| lastuserupdated | int | 4 |
| Num_Chamadas | int | 4 |
| ReverseCDR | int | 4 |
| FK_WNP_ID_CllgnNumber_Original | int | 4 |
| SMS_Length | int | 4 |
| Tipo_Servico_ID | int | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

