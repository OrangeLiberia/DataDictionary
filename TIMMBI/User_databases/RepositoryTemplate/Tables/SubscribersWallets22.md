#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > in.SubscribersWallets22

# ![Tables](../../../../Images/Table32.png) [in].[SubscribersWallets22]

---

## <a name="#description"></a>MS_Description

Subscriber Wallet Snapshot Day 22

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubscribersWallets22: AcountID\WalletTypeID](../../../../Images/pkcluster.png)](#indexes) | AcountID | int | 4 | NOT NULL | _IN Subscriber ID_ |
| [![Cluster Primary Key PK_SubscribersWallets22: AcountID\WalletTypeID](../../../../Images/pkcluster.png)](#indexes) | WalletTypeID | int | 4 | NOT NULL | _Wallet type ( ref. table [BI].[in].[WalletTypes] )_ |
|  | Balance | numeric(24,6) | 13 | NOT NULL | _Subscriber balance_ |
|  | LastBalanceUpdateDate | datetime | 8 | NOT NULL | _Date wehn balance was updated_ |
|  | DefiniteStatusID | int | 4 | NULL allowed |  |
|  | IN | tinyint | 1 | NOT NULL | _IN Identification (ref. table [BI].[in].[INs] )_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubscribersWallets22: AcountID\WalletTypeID](../../../../Images/pkcluster.png)](#indexes) | PK_SubscribersWallets22 | AcountID, WalletTypeID | YES | IN |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

