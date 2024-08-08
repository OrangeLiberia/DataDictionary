#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.AllBalance

# ![Tables](../../../../Images/Table32.png) [dbo].[AllBalance]

---

## <a name="#description"></a>MS_Description

List of all users and subscribers and their corresponding balance

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_STD_Balance](../../../../Images/Index.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_STD_Balance](../../../../Images/Index.png)](#indexes) | CurrencyType | varchar(16) | 16 | NULL allowed | _Currency (USD/LRD)_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_STD_Balance](../../../../Images/Index.png)](#indexes) | AccountType | varchar(15) | 15 | NULL allowed | _Type of user of accounts. e.g. Subscriber ,Channel User, etc.: Subscriber (eq. SUBSCRIBER), Channel User ( eq. CHANNEL), MERCHANT (mainly for 100 'Zebra' accounts), Bill Company (eq. WBILLMER), OM (eq. OPERATOR), Technical (eq. OPERATOR but for *IN* accounts).<br />IND01 (Stock Wallet) Main stock mWallet of MFS Owner, in which stock (issued by the bank) is created and all distribution of money points to the respective MFS Provider distribution system takes place. This wallet is created during factory setting and will be represented as MFS Owner in the Web tools.<br />IND02 (On the fly) MFS Owner mWallet which stores all the ‘On the Fly’ P2P transaction pending for confirmation from receiver.<br />IND03 (Service Charge & Commission) MFS Provider mWallet which stores all Service Charge and Commission charged during any transaction, also known as Earning Account (EA.) Each MFS Provider will have its own EA wallet.<br />IND04 (Stock Generation) This is a mWallet which provides sum of total Stock Generated in the mobiquity® system. It only has negative balance. This will be bank Ids against each transaction representing which bank this money is put into. This wallet will also be used as a bank pool for all banking related transactions_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | AccountID | varchar(32) | 32 | NULL allowed | _Unique ID of the user_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_STD_Balance](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(32) | 32 | NULL allowed | _MSISDN_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_STD_Balance](../../../../Images/Index.png)](#indexes) | Balance | numeric(17,2) | 9 | NULL allowed |  |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | UserName | varchar(80) | 80 | NULL allowed | _First Name of user_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | LastName | varchar(80) | 80 | NULL allowed | _Last name of user_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | UserDomain | varchar(50) | 50 | NULL allowed | _Domain of the user_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | UserCategory | varchar(50) | 50 | NULL allowed | _Category of the user_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | WalletNumber | varchar(25) | 25 | NULL allowed | _Identifier of the wallet_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | FrozenAmount | numeric(17,2) | 9 | NULL allowed | _Frozen amount on the user's wallet at the current time. This can be done while the transactions correction are processing_ |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_STD_Balance](../../../../Images/Index.png)](#indexes) | PaymentTypeID | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|---|
|  | IX_STD_Balance | RefDate, CurrencyType, MSISDN | AccountType, PaymentTypeID, Balance |  |  |  |  | pschSemesterPartition | RefDate |
| [![Cluster Key cci_AllBalanceEx: *](../../../../Images/cluster.png)](#indexes) | cci_AllBalanceEx |  | FileID, ID, RefDate, CurrencyType, AccountType, AccountID, MSISDN, Balance, UserName, LastName, UserDomain, UserCategory, WalletNumber, FrozenAmount, PaymentTypeID | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

