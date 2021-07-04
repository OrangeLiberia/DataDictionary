#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._MSISDN_IMEI_201604_2

# ![Tables](../../../../Images/Table32.png) [dbo].[_MSISDN_IMEI_201604_2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| MSISDN | varchar(32) | 32 | NOT NULL |
| ICCID | varchar(20) | 20 | NULL allowed |
| IMSI | varchar(20) | 20 | NULL allowed |
| IMEI | varchar(32) | 32 | NOT NULL |
| USIM | bit | 1 | NULL allowed |
| 3G | bit | 1 | NULL allowed |
| LTEDevice | bit | 1 | NULL allowed |
| IDTipoCartao | tinyint | 1 | NULL allowed |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

