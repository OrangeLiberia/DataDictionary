#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Views](Views.md) > msc.CallsMOAll

# ![Views](../../../../Images/View32.png) [msc].[CallsMOAll]

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
| DIALEDDIGITS | varchar(32) | 32 |
| CALLEDNUMBER_CC | varchar(6) | 6 |
| CALLEDNUMBER_NDC | varchar(6) | 6 |
| CHALLOCTIME | datetime | 8 |
| ANSWERTIME | datetime | 8 |
| DISCONNECTTIME | datetime | 8 |
| RELEASETIME | datetime | 8 |
| CLASSMARKTIME | datetime | 8 |
| OUTTRUNKSEIZURE | datetime | 8 |
| OUTTRUNKGROUP | int | 4 |
| CallDuration | int | 4 |
| CAUSEFORTERMINATION | smallint | 2 |
| DIAG_ERRCOD | smallint | 2 |
| MSCLASSMARK | varchar(32) | 32 |
| CALLINGSUBSCRIBERCAT | smallint | 2 |
| DurSecBill | int | 4 |
| RateDur | float | 8 |
| RateBill | float | 8 |
| RateIconRoam | float | 8 |
| AMSISDN | varchar(32) | 32 |
| BMSISDN | varchar(32) | 32 |
| StartTime | datetime | 8 |
| COSID | int | 4 |
| IDOrig | int | 4 |
| IDDest | int | 4 |
| IDTariff | int | 4 |
| IDTariffIconRoam | int | 4 |
| DuplicateCode | tinyint | 1 |
| MSC | tinyint | 1 |
| CalledIMEI | varchar(32) | 32 |
| CalledIMSI | varchar(32) | 32 |
| CellSectorID | int | 4 |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

