#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Views](Views.md) > msc.CallsTRAll

# ![Views](../../../../Images/View32.png) [msc].[CallsTRAll]

---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| FileID | bigint | 8 |
| CDRID | int | 4 |
| CALLINGNUMBER | varchar(32) | 32 |
| CALLEDNUMBER | varchar(32) | 32 |
| OUTTRUNKSEIZURE | datetime | 8 |
| ANSWERTIME | datetime | 8 |
| OUTTRUNKRELEASE | datetime | 8 |
| CAUSEFORTERMINATION | smallint | 2 |
| INTRUNKGROUP | int | 4 |
| OUTTRUNKGROUP | int | 4 |
| CallDuration | int | 4 |
| DurSecBill | int | 4 |
| RateDur | float | 8 |
| RateBill | float | 8 |
| RateIconRoam | float | 8 |
| AMSISDN | varchar(32) | 32 |
| BMSISDN | varchar(32) | 32 |
| StartTime | datetime | 8 |
| IDOrig | int | 4 |
| IDDest | int | 4 |
| IDTariff | int | 4 |
| IDTariffIconRoam | int | 4 |
| MSC | tinyint | 1 |
| DuplicateCode | tinyint | 1 |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

