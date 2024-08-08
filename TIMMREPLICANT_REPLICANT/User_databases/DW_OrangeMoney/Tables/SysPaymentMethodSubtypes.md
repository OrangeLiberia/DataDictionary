#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.SysPaymentMethodSubtypes

# ![Tables](../../../../Images/Table32.png) [dbo].[SysPaymentMethodSubtypes]

---

## <a name="#description"></a>MS_Description

Provide details of payment method subtypes.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SysPaymentMethodSubtypesv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_SysPaymentMethodSubtypesv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_SysPaymentMethodSubtypesv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | PAYMENT_METHOD_SUBTYPE_ID | varchar(10) | 10 | NULL allowed | _Payment method subtyp id_ |
|  | PAYMENT_METHOD_TYPE_ID | varchar(10) | 10 | NULL allowed | _Payment method type id_ |
|  | SUBTYPE_NAME | varchar(30) | 30 | NOT NULL | _Name of subtype_ |
|  | STATUS | varchar(3) | 3 | NULL allowed | _Status of payment subtype (eg. - Y for active or N for deleted.)_ |
|  | PAYMENT_TYPE_ID | int | 4 | NULL allowed | _Payment type id that belong to payment subtype_ |
|  | CREATED_BY | varchar(30) | 30 | NOT NULL | _Userid of the user who registered the payment subtype._ |
|  | CREATED_ON | datetime | 8 | NOT NULL | _Creation date_ |
|  | MODIFIED_BY | varchar(30) | 30 | NULL allowed | _Userid of the user who modified the payment subtype_ |
|  | MODIFIED_ON | datetime | 8 | NULL allowed | _Modification date_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SysPaymentMethodSubtypesv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_SysPaymentMethodSubtypesv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

