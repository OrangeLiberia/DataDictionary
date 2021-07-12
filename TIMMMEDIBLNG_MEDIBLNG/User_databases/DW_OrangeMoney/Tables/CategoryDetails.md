#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.CategoryDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[CategoryDetails]

---

## <a name="#description"></a>MS_Description

Contains details of all categories located in domains.

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
| [![Cluster Primary Key PK_CategoryDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_CategoryDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CategoryDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |  |
|  | CurrencyType | varchar(16) | 16 | NOT NULL |  |
|  | CATEGORY_CODE | varchar(10) | 10 | NOT NULL | _Category code of the user_ |
|  | DOMAIN_CODE | varchar(10) | 10 | NOT NULL | _Domain code of the user_ |
|  | CATEGORY_NAME | varchar(50) | 50 | NOT NULL | _Category Name of the user_ |
|  | PARENT_CATEGORY_CODE | varchar(10) | 10 | NULL allowed | _Category code of the parent_ |
|  | STATUS | varchar(2) | 2 | NOT NULL | _Status of the transfer control profile (Y = Activated, N = Deleted)_ |
|  | CATEGORY_TYPE | varchar(10) | 10 | NULL allowed | _Category type of the user_ |
|  | SEQUENCE_NO | numeric(10,0) | 9 | NULL allowed | _This is to identify the hierachy of categories (eg. To identify parent or child categories)_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CategoryDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_CategoryDetailsv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

