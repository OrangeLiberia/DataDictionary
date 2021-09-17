#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.MobileMoneyLECRequests

# ![Tables](../../../../Images/Table32.png) [dbo].[MobileMoneyLECRequests]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|
| ID | bigint | 8 | NOT NULL | 1 - 1 |  |
| MSISDN | varchar(20) | 20 | NULL allowed |  |  |
| Amount | float | 8 | NULL allowed |  |  |
| Currency | varchar(5) | 5 | NULL allowed |  |  |
| BillingID | varchar(20) | 20 | NULL allowed |  |  |
| MMTransID | varchar(20) | 20 | NULL allowed |  |  |
| EntryDT | datetime | 8 | NULL allowed |  | (getdate()) |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

