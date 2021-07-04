#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._OrangeCountersSCD1

# ![Tables](../../../../Images/Table32.png) [dbo].[_OrangeCountersSCD1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| DtYMD | varchar(10) | 10 | NOT NULL |
| Service | varchar(10) | 10 | NULL allowed |
| Destination | varchar(20) | 20 | NOT NULL |
| NSubs | int | 4 | NULL allowed |
| Qty | int | 4 | NULL allowed |
| Amount | float | 8 | NULL allowed |
| Minutes | numeric(26,6) | 13 | NULL allowed |
| NValidCalls | bigint | 8 | NULL allowed |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

