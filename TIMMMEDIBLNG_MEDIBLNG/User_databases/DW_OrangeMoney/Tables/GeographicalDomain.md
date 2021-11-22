#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.GeographicalDomain

# ![Tables](../../../../Images/Table32.png) [dbo].[GeographicalDomain]

---

## <a name="#description"></a>MS_Description

Provide the list and details of the geographical domains

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_GeographicalDomainv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_GeographicalDomainv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_GeographicalDomainv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | GRPH_DOMAIN_CODE | varchar(10) | 10 | NOT NULL | _Geographical domain code_ |
|  | NETWORK_NAME | varchar(50) | 50 | NOT NULL | _Network name in which user falls_ |
|  | PARENT_GRPH_DOMAIN_NAME | varchar(50) | 50 | NOT NULL | _Name of the parent graphical domain_ |
|  | PARENT_GRPH_DOMAIN_TYPE | varchar(10) | 10 | NOT NULL | _Type of the parent graphical domain(e.g. Zone,Area etc)_ |
|  | GRPH_DOMAIN_TYPE | varchar(10) | 10 | NOT NULL | _Type of the  graphical domain(e.g. Zone,Area etc)_ |
|  | GRPH_DOMAIN_SHORT_NAME | varchar(50) | 50 | NOT NULL | _Name of the parent graphical domain_ |
|  | DESCRIPTION | varchar(50) | 50 | NOT NULL | _Status of the graphical domain_ |
|  | STATUS | varchar(1) | 1 | NULL allowed | _Status of the transfer control profile (Y = Activated, N = Deleted). _ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_GeographicalDomainv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_GeographicalDomainv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

