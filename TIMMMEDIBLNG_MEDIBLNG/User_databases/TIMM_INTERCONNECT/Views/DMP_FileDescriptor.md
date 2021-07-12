#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Views](Views.md) > dbo.DMP_FileDescriptor

# ![Views](../../../../Images/View32.png) [dbo].[DMP_FileDescriptor]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | bigint | 8 |
| FileID | bigint | 8 |
| CommitCharge | int | 4 |
| FK_Central_ID | int | 4 |
| QOS_Processing | bit | 1 |
| ICON_Processing | int | 4 |
| CDR_Deleted | int | 4 |
| FirstCDRTime | datetime | 8 |
| LastCDRTime | datetime | 8 |
| DBName | varchar(50) | 50 |
| ICON_Reprocessing | int | 4 |
| ProcessError | int | 4 |
| ReprocessError | int | 4 |
| SMS_Processing | int | 4 |
| SMS_Reprocessing | int | 4 |
| SMS_ProcessError | int | 4 |
| SMS_ReprocessError | int | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

