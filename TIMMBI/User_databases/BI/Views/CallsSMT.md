#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Views](Views.md) > msc.CallsSMT

# ![Views](../../../../Images/View32.png) [msc].[CallsSMT]

---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| FileID | bigint | 8 |
| CDRID | int | 4 |
| IMSI | varchar(32) | 32 |
| IMEI | varchar(32) | 32 |
| CALLINGNUMBER | varchar(32) | 32 |
| CALLINGNUMBER_CC | varchar(6) | 6 |
| CALLINGNUMBER_NDC | varchar(6) | 6 |
| CALLEDNUMBER | varchar(32) | 32 |
| CALLEDNUMBER_CC | varchar(6) | 6 |
| CALLEDNUMBER_NDC | varchar(6) | 6 |
| DISCONNECTTIME | datetime | 8 |
| RELEASETIME | datetime | 8 |
| CAUSEFORTERMINATION | smallint | 2 |
| AMSISDN | varchar(32) | 32 |
| BMSISDN | varchar(32) | 32 |
| StartTime | datetime | 8 |
| IDOrig | int | 4 |
| IDDest | int | 4 |
| IDTariff | int | 4 |
| MSC | tinyint | 1 |
| DuplicateCode | tinyint | 1 |
| CellSectorID | int | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

