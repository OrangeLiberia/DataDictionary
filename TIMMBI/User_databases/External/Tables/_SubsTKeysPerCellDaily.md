#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._SubsTKeysPerCellDaily

# ![Tables](../../../../Images/Table32.png) [dbo].[_SubsTKeysPerCellDaily]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| MSISDN | varchar(20) | 20 | NULL allowed |
| IDDimDate | int | 4 | NULL allowed |
| Day | varchar(10) | 10 | NOT NULL |
| TransactionKey | int | 4 | NOT NULL |
| WalletID | int | 4 | NOT NULL |
| CellID | int | 4 | NOT NULL |
| Qty | int | 4 | NULL allowed |
| Amount | numeric(38,6) | 17 | NULL allowed |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

