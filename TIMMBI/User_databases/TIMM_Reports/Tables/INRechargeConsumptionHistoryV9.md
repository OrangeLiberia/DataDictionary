#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.INRechargeConsumptionHistoryV9

# ![Tables](../../../../Images/Table32.png) [dbo].[INRechargeConsumptionHistoryV9]

---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__INRechar__3214EC27DF68E058: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | WalletID | varchar(10) | 10 | NULL allowed |  |
|  | WalletName | varchar(32) | 32 | NULL allowed |  |
|  | DayHour | datetime | 8 | NULL allowed |  |
|  | Hour | varchar(10) | 10 | NULL allowed |  |
|  | Recharged | varchar(32) | 32 | NULL allowed |  |
|  | RechargedInc | varchar(32) | 32 | NULL allowed |  |
|  | Consumed | varchar(32) | 32 | NULL allowed |  |
|  | ConsumedInc | varchar(32) | 32 | NULL allowed |  |
|  | LastDayRemainingBalance | varchar(32) | 32 | NULL allowed |  |
|  | LastDayRechargedBalance | varchar(32) | 32 | NULL allowed |  |
|  | LastDayConsumed | varchar(32) | 32 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__INRechar__3214EC27DF68E058: ID](../../../../Images/pkcluster.png)](#indexes) | PK__INRechar__3214EC27DF68E058 | ID | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

