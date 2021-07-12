#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.RecieverKYC

# ![Tables](../../../../Images/Table32.png) [dbo].[RecieverKYC]

---

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
| [![Cluster Primary Key PK_RecieverKYCv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_RecieverKYCv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_RecieverKYCv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
|  | CurrencyType | varchar(16) | 16 | NOT NULL |
|  | TNO_MSIDN | varchar(15) | 15 | NULL allowed |
|  | TNO_ID | varchar(30) | 30 | NOT NULL |
|  | UNREG_FIRST_NAME | varchar(80) | 80 | NULL allowed |
|  | UNREG_LAST_NAME | varchar(80) | 80 | NULL allowed |
|  | UNREG_DOB | datetime | 8 | NULL allowed |
|  | UNREG_ID_NUMBER | varchar(15) | 15 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_RecieverKYCv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_RecieverKYCv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

