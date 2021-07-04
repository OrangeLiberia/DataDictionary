#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.BHPMSCCallsMT

# ![Tables](../../../../Images/Table32.png) [dbo].[BHPMSCCallsMT]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| FileID | bigint | 8 | NOT NULL |
| CDRID | int | 4 | NOT NULL |
| IMSI | varchar(32) | 32 | NULL allowed |
| IMEI | varchar(32) | 32 | NULL allowed |
| CallingNumber | varchar(32) | 32 | NULL allowed |
| CalledNumber | varchar(32) | 32 | NULL allowed |
| DialedDigits | varchar(32) | 32 | NULL allowed |
| CallDuration | int | 4 | NULL allowed |
| CHALLOCTIME | datetime | 8 | NULL allowed |
| ANSWERTIME | datetime | 8 | NULL allowed |
| DISCONNECTTIME | datetime | 8 | NULL allowed |
| RELEASETIME | datetime | 8 | NULL allowed |
| INTRUNKSEIZURE | datetime | 8 | NULL allowed |
| INTRUNKGROUP | int | 4 | NULL allowed |
| CAUSEFORTERMINATION | smallint | 2 | NULL allowed |
| DIAG_ERRCOD | smallint | 2 | NULL allowed |
| ReleaseCause | varchar(100) | 100 | NULL allowed |
| Cell_SAC_ID | int | 4 | NULL allowed |
| SiteName | varchar(50) | 50 | NULL allowed |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

