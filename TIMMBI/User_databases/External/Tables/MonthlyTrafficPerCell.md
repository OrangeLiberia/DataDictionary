#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.MonthlyTrafficPerCell

# ![Tables](../../../../Images/Table32.png) [dbo].[MonthlyTrafficPerCell]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| IDDimDate | int | 4 | NOT NULL |
| Month | datetime | 8 | NOT NULL |
| IDOrig | int | 4 | NOT NULL |
| IDDest | int | 4 | NOT NULL |
| ProductType | int | 4 | NOT NULL |
| WalletType | int | 4 | NOT NULL |
| CellID | int | 4 | NOT NULL |
| NCalls | int | 4 | NOT NULL |
| NCallsAttempts | int | 4 | NOT NULL |
| NChrgCalls | int | 4 | NOT NULL |
| NFreeCalls | int | 4 | NOT NULL |
| ChrgdDurSec | int | 4 | NOT NULL |
| FreeDurSec | int | 4 | NOT NULL |
| Amount | float | 8 | NOT NULL |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

