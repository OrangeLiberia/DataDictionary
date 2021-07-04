#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._Subs_USIM_LTE

# ![Tables](../../../../Images/Table32.png) [dbo].[_Subs_USIM_LTE]

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
| ServicoID | numeric(18,0) | 9 | NULL allowed |
| ICCID | varchar(20) | 20 | NULL allowed |
| IMSI | varchar(20) | 20 | NULL allowed |
| IMEI | varchar(20) | 20 | NULL allowed |
| LTEFeature | bit | 1 | NULL allowed |
| USIM | bit | 1 | NULL allowed |
| LTEDevice | bit | 1 | NULL allowed |
| Status | int | 4 | NULL allowed |
| IDDimDate | int | 4 | NULL allowed |
| ExecDT | date | 3 | NULL allowed |
| APP | varchar(20) | 20 | NULL allowed |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

