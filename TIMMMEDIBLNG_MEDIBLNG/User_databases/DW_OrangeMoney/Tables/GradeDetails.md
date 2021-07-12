#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.GradeDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[GradeDetails]

---

## <a name="#description"></a>MS_Description

Provides the list of user grades and the corresponding category code

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
| [![Cluster Primary Key PK_GradeDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_GradeDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_GradeDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | GRADE_CODE | varchar(10) | 10 | NOT NULL | _Grade code_ |
|  | GRADE_NAME | varchar(40) | 40 | NOT NULL | _Grade name_ |
|  | CATEGORY_CODE | varchar(10) | 10 | NOT NULL | _Category code_ |
|  | STATUS | varchar(1) | 1 | NOT NULL | _Status of the Grade : always = Y (Y = Activated, N = Deleted)_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_GradeDetailsv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_GradeDetailsv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

