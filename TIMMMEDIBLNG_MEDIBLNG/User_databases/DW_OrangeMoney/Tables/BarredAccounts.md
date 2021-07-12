#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.BarredAccounts

# ![Tables](../../../../Images/Table32.png) [dbo].[BarredAccounts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_BarredAccountsv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_BarredAccountsv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_BarredAccountsv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | ACTION | varchar(5) | 5 | NOT NULL | _This represend whether displayed value is for BAR or UNBAR._ |
|  | SYS_TIMESTAMP | datetime | 8 | NULL allowed | _Time when user was bared/unbared_ |
|  | MSISDN | varchar(15) | 15 | NOT NULL | _MSISDN of user_ |
|  | PARTY_USER_ID | varchar(30) | 30 | NULL allowed | _User Id of the party._ |
|  | USER_NAME | varchar(180) | 180 | NOT NULL | _User name_ |
|  | PARENT_NAME | varchar(180) | 180 | NOT NULL | _Parent user name_ |
|  | PARTY_LOGIN_ID | varchar(20) | 20 | NULL allowed | _Party login id_ |
|  | TYPE | varchar(70) | 70 | NULL allowed | _Barring/Unbarring type. (eg. Receiver, Sender, Both)_ |
|  | BARRING_REASON | varchar(50) | 50 | NULL allowed | _Barred reason_ |
|  | ACTION_PERFORMED_BY | varchar(180) | 180 | NULL allowed | _Identification who did the action of Barred/Unbarred_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_BarredAccountsv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_BarredAccountsv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

