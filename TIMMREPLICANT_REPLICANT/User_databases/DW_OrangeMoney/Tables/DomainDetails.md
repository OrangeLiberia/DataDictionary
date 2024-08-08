#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.DomainDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[DomainDetails]

---

## <a name="#description"></a>MS_Description

Provides the list of all user domains and details

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DomainDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_DomainDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_DomainDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | DOMAIN_CODE | varchar(10) | 10 | NULL allowed | _Domain code of the user. _ |
|  | DOMAIN_NAME | varchar(50) | 50 | NULL allowed | _Domain Name of the user. _ |
|  | DOMAIN_TYPE_CODE | varchar(10) | 10 | NULL allowed | _domain type code of the user. _ |
|  | STATUS | varchar(2) | 2 | NULL allowed | _Status of the transfer control profile (Y = Activated, N = Deleted). _ |
|  | OWNER_CATEGORY | varchar(11) | 11 | NULL allowed | _Owner category. _ |
|  | NUM_OF_CATEGORIES | numeric(5,0) | 5 | NULL allowed | _Number of catagories belongs to the domain. _ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DomainDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_DomainDetailsv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

