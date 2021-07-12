#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.AuditPinModified

# ![Tables](../../../../Images/Table32.png) [dbo].[AuditPinModified]

---

## <a name="#description"></a>MS_Description

Display Audit Trail records in a specified date range

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_AuditPinModifiedv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_AuditPinModifiedv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_AuditPinModifiedv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
|  | CurrencyType | varchar(16) | 16 | NULL allowed |
|  | USER_ID | varchar(20) | 20 | NOT NULL |
|  | USER_NAME | varchar(180) | 180 | NOT NULL |
|  | CATEGORY_CODE | varchar(10) | 10 | NOT NULL |
|  | MSISDN | varchar(15) | 15 | NULL allowed |
|  | LAST_NAME | varchar(80) | 80 | NULL allowed |
|  | USER_TYPE | varchar(10) | 10 | NULL allowed |
|  | TRANSACTION_ON | datetime | 8 | NULL allowed |
|  | STATUS | varchar(2) | 2 | NULL allowed |
|  | ERROR_CODE | varchar(20) | 20 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_AuditPinModifiedv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_AuditPinModifiedv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

