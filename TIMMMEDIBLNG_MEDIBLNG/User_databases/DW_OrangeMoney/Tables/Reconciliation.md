#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.Reconciliation

# ![Tables](../../../../Images/Table32.png) [dbo].[Reconciliation]

---

## <a name="#description"></a>MS_Description

Provides the balance for the OM bank and for each user type. Check if the accounts are balanced

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Reconciliationv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_Reconciliationv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_Reconciliationv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | PROVIDER_NAME | varchar(80) | 80 | NOT NULL | _Orange Money. _ |
|  | STOCK_CREATED | numeric(19,0) | 9 | NOT NULL | _Total amount of stock created in the system. _ |
|  | TAX_CREATED_TA | numeric(19,0) | 9 | NULL allowed | _Total Tax collected on transaction amt. _ |
|  | TAX_CRATED_SC | numeric(19,0) | 9 | NULL allowed | _Total Tax collected on service charge. _ |
|  | TAX_CREATED_COMM | numeric(19,0) | 9 | NULL allowed | _Total Tax collected on commission. _ |
|  | ONTHEFLY_SERVCHRG | numeric(19,0) | 9 | NULL allowed | _Total on the fly service charge. _ |
|  | BANK | numeric(19,0) | 9 | NULL allowed | _Total stock available in the system. _ |
|  | ORANGE | numeric(19,0) | 9 | NULL allowed | _Total service charge in the system. _ |
|  | ON_THE_FLY | numeric(19,0) | 9 | NULL allowed |  |
|  | ORANGE_IMT | numeric(19,0) | 9 | NULL allowed | _IMT account balance for the WU. _ |
|  | SUBSCRIBERS | numeric(19,0) | 9 | NULL allowed | _Total balance of all the subscriber. _ |
|  | CHANNEL_USERS | numeric(19,0) | 9 | NULL allowed | _Total balance of all the channel users. _ |
|  | MERCHANTS | numeric(19,0) | 9 | NULL allowed | _Total balance of the merchant. _ |
|  | BREAKAGE_BALANCE | numeric(19,0) | 9 | NULL allowed | _Not Used in Orange. _ |
|  | INT_REMIT | numeric(19,0) | 9 | NULL allowed |  |
|  | TOTAL_BAL | numeric(19,0) | 9 | NULL allowed |  |
|  | UNKNOWN01 | varchar(max) | max | NULL allowed |  |
|  | UNKNOWN02 | varchar(max) | max | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Reconciliationv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_Reconciliationv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

