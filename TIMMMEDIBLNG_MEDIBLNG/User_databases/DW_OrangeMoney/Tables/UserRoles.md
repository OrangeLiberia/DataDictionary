#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.UserRoles

# ![Tables](../../../../Images/Table32.png) [dbo].[UserRoles]

---

## <a name="#description"></a>MS_Description

Provide details of group roles and the category they belongs to

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
| [![Cluster Primary Key PK_UserRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_UserRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_UserRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | USERID | varchar(50) | 50 | NOT NULL | _User ID_ |
|  | GATEWAY_TYPES | varchar(50) | 50 | NOT NULL | _Gateway type. (eg.WEB, USSD)_ |
|  | GROUP_ROLE_CODE | varchar(38) | 38 | NOT NULL | _Group role code for user id_ |
|  | CREATED_BY | varchar(20) | 20 | NULL allowed | _Userid of the user who registered the user_ |
|  | CREATED_ON | datetime | 8 | NULL allowed | _Creation date_ |
|  | MODIFIED_BY | varchar(20) | 20 | NULL allowed | _Userid of the user who modified the user_ |
|  | MODIFIED_ON | datetime | 8 | NULL allowed | _Modification date_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_UserRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_UserRolesv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

