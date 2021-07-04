#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.BHPINCalls

# ![Tables](../../../../Images/Table32.png) [dbo].[BHPINCalls]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| SubsNumber | varchar(50) | 50 | NULL allowed |
| OriginDigits | varchar(50) | 50 | NULL allowed |
| DialedDigits | varchar(50) | 50 | NULL allowed |
| AMSISDN | varchar(50) | 50 | NULL allowed |
| BMSISDN | varchar(50) | 50 | NULL allowed |
| IDOrig | int | 4 | NULL allowed |
| IDDest | int | 4 | NULL allowed |
| StartTime | datetime | 8 | NULL allowed |
| OriginateTime | datetime | 8 | NULL allowed |
| AnswerTime | datetime | 8 | NULL allowed |
| DisconnectTime | datetime | 8 | NULL allowed |
| ProductType | int | 4 | NOT NULL |
| DurSec | int | 4 | NULL allowed |
| ChargeableDuration | int | 4 | NULL allowed |
| AmountCharged | float | 8 | NULL allowed |
| RateDur | float | 8 | NULL allowed |
| EndingBalance | float | 8 | NULL allowed |
| WalletType | int | 4 | NULL allowed |
| PI | bit | 1 | NOT NULL |
| ServiceAccessCode | varchar(20) | 20 | NULL allowed |
| IN | tinyint | 1 | NOT NULL |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

