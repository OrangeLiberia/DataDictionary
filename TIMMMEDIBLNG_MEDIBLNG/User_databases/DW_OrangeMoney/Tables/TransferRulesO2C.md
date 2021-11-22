#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.TransferRulesO2C

# ![Tables](../../../../Images/Table32.png) [dbo].[TransferRulesO2C]

---

## <a name="#description"></a>MS_Description

Provides the list of the transfer rules between the operators and the channel-users.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferRulesO2Cv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_TransferRulesO2Cv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_TransferRulesO2Cv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | TRANSFER_RULE_ID | numeric(10,0) | 9 | NOT NULL | _Unique Identifier of the Transfer rule_ |
|  | PAYEE_DOMAIN_CODE | varchar(10) | 10 | NOT NULL | _Domain code of the payee_ |
|  | PAYEE_CATEGORY_CODE | varchar(10) | 10 | NOT NULL | _Category code of the payee_ |
|  | APPROVAL_LIMIT_1 | numeric(19,0) | 9 | NOT NULL | _Limit of transfer amount for which approval1 is required_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferRulesO2Cv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_TransferRulesO2Cv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

