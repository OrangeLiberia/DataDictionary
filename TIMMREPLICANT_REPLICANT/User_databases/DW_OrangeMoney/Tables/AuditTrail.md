#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.AuditTrail

# ![Tables](../../../../Images/Table32.png) [dbo].[AuditTrail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | CurrencyType | varchar(16) | 16 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_ID | varchar(32) | 32 | NOT NULL |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Cust_ID | varchar(32) | 32 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | USER_ID | varchar(32) | 32 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | User_Access_ID | varchar(60) | 60 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | SERVICE_TYPE | varchar(10) | 10 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_SUBTYPE | varchar(10) | 10 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Account1 | varchar(32) | 32 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Account2 | varchar(32) | 32 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Transaction_Status | varchar(3) | 3 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Transaction_Date | datetime | 8 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Transaction_On | datetime | 8 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ERROR_CODE | varchar(20) | 20 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Comments | varchar(256) | 256 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ATT_1_NAME | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ATT_1_VALUE | varchar(128) | 128 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ATT_2_NAME | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ATT_2_VALUE | varchar(128) | 128 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ATT_3_NAME | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | ATT_3_VALUE | varchar(128) | 128 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Sender_MFS_Provider | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Sender_Payment_Instrument | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Sender_Wallet_Type | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Sender_Linked_Bank | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Receiver_MFS_Provider | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Receiver_Payment_Instrument | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Receiver_Wallet_Type | varchar(64) | 64 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Receiver_Linked_Bank | varchar(256) | 256 | NULL allowed |
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | Transaction_Mode | varchar(512) | 512 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|
| [![Cluster Key cci_AuditTrailv1: *](../../../../Images/cluster.png)](#indexes) | cci_AuditTrailv1 | FileID, ID, RefDate, CurrencyType, TRANSACTION_ID, Cust_ID, USER_ID, User_Access_ID, SERVICE_TYPE, TRANSFER_SUBTYPE, Account1, Account2, Transaction_Status, Transaction_Date, Transaction_On, ERROR_CODE, Comments, ATT_1_NAME, ATT_1_VALUE, ATT_2_NAME, ATT_2_VALUE, ATT_3_NAME, ATT_3_VALUE, Sender_MFS_Provider, Sender_Payment_Instrument, Sender_Wallet_Type, Sender_Linked_Bank, Receiver_MFS_Provider, Receiver_Payment_Instrument, Receiver_Wallet_Type, Receiver_Linked_Bank, Transaction_Mode | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

