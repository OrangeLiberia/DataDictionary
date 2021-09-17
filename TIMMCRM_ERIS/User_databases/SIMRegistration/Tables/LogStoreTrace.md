#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.LogStoreTrace

# ![Tables](../../../../Images/Table32.png) [dbo].[LogStoreTrace]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|
| ID | int | 4 | NULL allowed |  |
| MSISDN | varchar(32) | 32 | NULL allowed |  |
| UserID | int | 4 | NULL allowed |  |
| Status | int | 4 | NULL allowed |  |
| IID | varchar(64) | 64 | NULL allowed |  |
| MID | varchar(64) | 64 | NULL allowed |  |
| ElapsedSeconds | int | 4 | NULL allowed |  |
| Dt | datetime | 8 | NULL allowed | (getdate()) |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

