#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.RechargeConsumptionHistory

# ![Tables](../../../../Images/Table32.png) [dbo].[RechargeConsumptionHistory]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_RechargeConsumptionHistory: RefDate\Currency](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
| [![Cluster Primary Key PK_RechargeConsumptionHistory: RefDate\Currency](../../../../Images/pkcluster.png)](#indexes) | Currency | varchar(8) | 8 | NOT NULL |
|  | Recharged | decimal(18,2) | 9 | NOT NULL |
|  | Consumed | decimal(18,2) | 9 | NOT NULL |
|  | Remaining Balance | decimal(18,2) | 9 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_RechargeConsumptionHistory: RefDate\Currency](../../../../Images/pkcluster.png)](#indexes) | PK_RechargeConsumptionHistory | RefDate, Currency | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

