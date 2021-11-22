#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.OnlineRechargesDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[OnlineRechargesDetails]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_OnlineRechargesDetails_ID: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_OnlineRechargesDetails_1](../../../../Images/Index.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |  |
| [![Indexes IX_OnlineRechargesDetails_2](../../../../Images/Index.png)](#indexes) | UserName | varchar(50) | 50 | NOT NULL |  |  |
| [![Indexes IX_OnlineRechargesDetails_1](../../../../Images/Index.png)](#indexes) | CompanyName | varchar(50) | 50 | NOT NULL |  |  |
| [![Indexes IX_OnlineRechargesDetails_2](../../../../Images/Index.png)](#indexes) | DateTime | datetime | 8 | NOT NULL |  |  |
| [![Indexes IX_OnlineRechargesDetails_1
IX_OnlineRechargesDetails_2](../../../../Images/Index.png)](#indexes)(2) | MSISDN | varchar(20) | 20 | NOT NULL |  |  |
|  | Amount | float | 8 | NOT NULL |  |  |
|  | InitialBalance | float | 8 | NULL allowed |  |  |
|  | FinalBalance | float | 8 | NULL allowed |  |  |
|  | TrKey | int | 4 | NOT NULL |  |  |
|  | WalletID | int | 4 | NOT NULL |  |  |
|  | ReferenceNumber | int | 4 | NULL allowed |  |  |
|  | BMSISDN | varchar(20) | 20 | NULL allowed |  |  |
|  | BWalletID | int | 4 | NULL allowed |  |  |
|  | IDPair | bigint | 8 | NULL allowed |  |  |
|  | StatusPair | int | 4 | NULL allowed |  | ((0)) |
|  | IDAPI | bigint | 8 | NULL allowed |  |  |
|  | StatusAPI | int | 4 | NULL allowed |  | ((0)) |
|  | ExternalID | varchar(50) | 50 | NULL allowed |  |  |
|  | TypeAPI | varchar(10) | 10 | NULL allowed |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_OnlineRechargesDetails_ID: ID](../../../../Images/pkcluster.png)](#indexes) | PK_OnlineRechargesDetails_ID | ID | YES |
|  | IX_OnlineRechargesDetails_1 | IDDimDate, CompanyName, MSISDN |  |
|  | IX_OnlineRechargesDetails_2 | UserName, DateTime, MSISDN |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

