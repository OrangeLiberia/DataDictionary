#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.Roles

# ![Tables](../../../../Images/Table32.png) [dbo].[Roles]

---

## <a name="#description"></a>MS_Description

Provide list of roles, corresponding domain types and groups including other role properties.

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
| [![Cluster Primary Key PK_Rolesv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_Rolesv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_Rolesv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | DOMAIN_TYPE | varchar(10) | 10 | NOT NULL | _Domain type code. Possible values can be found from domain detail export_ |
|  | ROLE_CODE | varchar(20) | 20 | NOT NULL | _Unique code for each domain_type_ |
|  | ROLE_NAME | varchar(60) | 60 | NOT NULL | _Description corresponding to role_code_ |
|  | GROUP_NAME | varchar(30) | 30 | NOT NULL | _Group name for role defined in GroupRoles export_ |
|  | STATUS | varchar(1) | 1 | NULL allowed | _Status of role. (eg. - Y for active or N for deleted.)_ |
|  | GATEWAY_TYPES | varchar(50) | 50 | NOT NULL | _Gateway type. (eg.WEB, USSD)_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Rolesv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_Rolesv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

