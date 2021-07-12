#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.AdminAuditTrail

# ![Tables](../../../../Images/Table32.png) [dbo].[AdminAuditTrail]

---

## <a name="#description"></a>MS_Description

Display Admit Audit Trail records in a specified date range

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
| [![Cluster Primary Key PK_AdminAuditTrailv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_AdminAuditTrailv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_AdminAuditTrailv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
|  | CurrencyType | varchar(16) | 16 | NULL allowed |
|  | USER_ID | varchar(32) | 32 | NULL allowed |
|  | USER_MSISDN | varchar(60) | 60 | NULL allowed |
|  | LOGGED_IN | datetime | 8 | NULL allowed |
|  | LOG_OUT | datetime | 8 | NULL allowed |
|  | CATEGORY | varchar(32) | 32 | NULL allowed |
|  | ACTION_TYPE | varchar(128) | 128 | NULL allowed |
|  | ACTION_PERFORMED_ON | varchar(32) | 32 | NULL allowed |
|  | BARRED_USER | varchar(32) | 32 | NULL allowed |
|  | REMARKS | varchar(256) | 256 | NULL allowed |
|  | CREATED_BY | varchar(20) | 20 | NULL allowed |
|  | CREATED_ON | datetime | 8 | NULL allowed |
|  | ATT_1_NAME | varchar(64) | 64 | NULL allowed |
|  | ATT_1_VALUE | varchar(128) | 128 | NULL allowed |
|  | ATT_2_NAME | varchar(64) | 64 | NULL allowed |
|  | ATT_2_VALUE | varchar(128) | 128 | NULL allowed |
|  | ATT_3_NAME | varchar(64) | 64 | NULL allowed |
|  | ATT_3_VALUE | varchar(128) | 128 | NULL allowed |
|  | SN | varchar(32) | 32 | NULL allowed |
|  | TRANSACTION_ID | varchar(32) | 32 | NULL allowed |
|  | Cust_ID | varchar(32) | 32 | NULL allowed |
|  | STATUS_ID | varchar(2) | 2 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_AdminAuditTrailv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_AdminAuditTrailv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

