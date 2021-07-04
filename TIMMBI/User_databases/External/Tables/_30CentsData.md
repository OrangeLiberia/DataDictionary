#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._30CentsData

# ![Tables](../../../../Images/Table32.png) [dbo].[_30CentsData]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| IDDimDate | int | 4 | NULL allowed |
| Day | datetime | 8 | NULL allowed |
| MSISDN | varchar(32) | 32 | NULL allowed |
| 30centsPurchases | int | 4 | NOT NULL |
| 30centsAmount | float | 8 | NOT NULL |
| SCRechargeTimes | int | 4 | NOT NULL |
| SCRechargeAmount | float | 8 | NOT NULL |
| OtherRechargesTimes | int | 4 | NOT NULL |
| OtherRechargesAmount | float | 8 | NOT NULL |
| 143Purchases | int | 4 | NOT NULL |
| 143Amount | float | 8 | NOT NULL |
| OtherPurchases | int | 4 | NOT NULL |
| OtherPurchasesAmount | float | 8 | NOT NULL |
| DataMB | numeric(33,12) | 17 | NOT NULL |
| TotalConsumedAmount | float | 8 | NOT NULL |
| SMSConsumedAmount | float | 8 | NOT NULL |
| VoiceConsumedAmount | float | 8 | NOT NULL |
| DataConsumedAmount | float | 8 | NOT NULL |
| VoiceConsumedOnNet | float | 8 | NOT NULL |
| VoiceConsumedOffNet | float | 8 | NOT NULL |
| VoiceConsumedIntl | float | 8 | NOT NULL |
| SMSConsumedOnNet | float | 8 | NOT NULL |
| SMSConsumedOffNet | float | 8 | NOT NULL |
| SMSConsumedIntl | float | 8 | NOT NULL |
| OnNetSeconds | bigint | 8 | NOT NULL |
| OffNetSeconds | bigint | 8 | NOT NULL |
| IntlSeconds | bigint | 8 | NOT NULL |
| OnNetSMS | bigint | 8 | NOT NULL |
| OffNetSMS | bigint | 8 | NOT NULL |
| IntlSMS | bigint | 8 | NOT NULL |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

