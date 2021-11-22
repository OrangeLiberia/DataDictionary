#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.Wallet

# ![Tables](../../../../Images/Table32.png) [dbo].[Wallet]

---

## <a name="#description"></a>MS_Description

The wallet contains the amount of the subscribers and Wallet Specifications.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Walletv1: *](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_WALLET_NUMBER](../../../../Images/Index.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_Walletv1: *](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_WALLET_NUMBER](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_Walletv1: *](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_WALLET_NUMBER](../../../../Images/Index.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
| [![Indexes IX_WALLET_NUMBER](../../../../Images/Index.png)](#indexes) | WALLET_NUMBER | varchar(20) | 20 | NOT NULL | _Wallet number in the system updated during the period_ |
|  | MSISDN | varchar(60) | 60 | NULL allowed | _MSISDN corresponding to wallet._ |
|  | VALID_FROM_DATE | datetime | 8 | NULL allowed | _Date from when wallet will be active_ |
|  | EXPIRY_DATE | datetime | 8 | NULL allowed | _Expiry date of wallet._ |
|  | CREATED_BY | varchar(30) | 30 | NOT NULL | _User id of the user who created the wallet_ |
|  | CREATED_ON | datetime | 8 | NOT NULL | _Wallet creation date_ |
|  | MODIFIED_ON | datetime | 8 | NOT NULL | _Wallet last modification date_ |
|  | LAST_TRANSFER_ON | datetime | 8 | NULL allowed | _Date when last transfer occurred for the wallet_ |
|  | LAST_TRANSFER_TYPE | varchar(20) | 20 | NULL allowed | _Type of last transfer for the wallet_ |
|  | ENCRYPTION_DONE | varchar(1) | 1 | NULL allowed | _Flag to decide whether encryption is done or not_ |
|  | WALLET_LOCK | varchar(1) | 1 | NULL allowed | _Flag to decide whether wallet is locked or not_ |
|  | IS_PRIMARY | varchar(1) | 1 | NULL allowed | _Flag to decide whether wallet is primary or not_ |
|  | PAYMENT_METHOD_TYPE_ID | varchar(20) | 20 | NULL allowed | _Payment method type id. Mapping of values can be find in SysPaymentmethod export_ |
|  | PAYMENT_METHOD_TYPE | varchar(50) | 50 | NULL allowed |  |
|  | PAYMENT_TYPE_ID | varchar(20) | 20 | NULL allowed | _Payment  type id. Mapping of values can be find in SysPaymentmethod export_ |
|  | USER_WALLET_TYPE | varchar(20) | 20 | NULL allowed | _Type of the Wallet. For *IND* accounts its value is DUMMY and for all others : for the first wallet the value is Normal and for other wallets it can be IRT or other custom value_ |
|  | PROVIDER_ID | varchar(20) | 20 | NULL allowed | _Provider id for wallet belongs._ |
|  | STATUS | varchar(30) | 30 | NULL allowed | _Wallet status can be Active(‘Y’), Deleted(‘N’), Suspended(‘S’), Add Initiated(AI) and Suspend Initiated(SI). In case of Suspend initiated wallet is considered as active._ |
|  | USER_GRADE | varchar(10) | 10 | NULL allowed | _User grade of the user belonging to the wallet._ |
|  | USERID | varchar(20) | 20 | NULL allowed | _User Id of the user belonging to the wallet_ |
|  | USER_TYPE | varchar(15) | 15 | NULL allowed | _User type of the user belonging to the wallet_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique | Compression | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Walletv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_Walletv1 | FileID, ID, RefDate |  | YES | PAGE ON PARTITIONS (1), PAGE ON PARTITIONS (2), PAGE ON PARTITIONS (3), PAGE ON PARTITIONS (4), PAGE ON PARTITIONS (5), PAGE ON PARTITIONS (6), PAGE ON PARTITIONS (7), PAGE ON PARTITIONS (8), PAGE ON PARTITIONS (9), PAGE ON PARTITIONS (10), PAGE ON PARTITIONS (11), PAGE ON PARTITIONS (12), PAGE ON PARTITIONS (13) | pschSemesterPartition | RefDate |
|  | IX_WALLET_NUMBER | WALLET_NUMBER | FileID, ID, RefDate |  |  | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

