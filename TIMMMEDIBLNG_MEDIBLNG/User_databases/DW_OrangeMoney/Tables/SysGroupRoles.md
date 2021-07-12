#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.SysGroupRoles

# ![Tables](../../../../Images/Table32.png) [dbo].[SysGroupRoles]

---

## <a name="#description"></a>MS_Description

Provide details of group roles and the category they belongs to.

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
| [![Cluster Primary Key PK_SysGroupRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_SysGroupRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_SysGroupRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | CATEGORY_CODE | varchar(10) | 10 | NOT NULL | _Category code for which group role is associated. Possible values for category details can be check in CategoryDetail export_ |
|  | GROUP_ROLE_CODE | varchar(38) | 38 | NOT NULL | _Group role code associated with category code_ |
|  | STATUS | varchar(1) | 1 | NULL allowed | _Status of group role (eg. - Y for active or N for deleted.)_ |
|  | GROUP_ROLE_NAME | varchar(38) | 38 | NULL allowed | _Description of GROUP_ROLE_CODE._ |
|  | GROUP_ROLE_TYPE | varchar(35) | 35 | NULL allowed | _Type of group role. (eg. Web, Wallet)_ |
|  | PAYMENT_TYPE_ID | int | 4 | NULL allowed | _Payment type ID. Mapping of payment type ID can be found in SysPaymentmethodSubtypes export._ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SysGroupRolesv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_SysGroupRolesv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

