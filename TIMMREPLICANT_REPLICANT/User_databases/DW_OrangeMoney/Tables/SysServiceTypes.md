#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.SysServiceTypes

# ![Tables](../../../../Images/Table32.png) [dbo].[SysServiceTypes]

---

## <a name="#description"></a>MS_Description

Provide list of service types available into the system.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SysServiceTypesv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_SysServiceTypesv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_SysServiceTypesv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | SERVICE_TYPE | varchar(20) | 20 | NOT NULL | _Service type_ |
|  | SERVICE_NAME | varchar(50) | 50 | NOT NULL | _Service type description corresponding to service type_ |
|  | STATUS_ID | varchar(2) | 2 | NULL allowed | _Status of service type. (eg. - Y for active or N for deleted.)_ |
|  | DISPLAY_ALLOWED | varchar(1) | 1 | NULL allowed | _Value decided whether service type should be displayed or not_ |
|  | IS_FINANCIAL | varchar(1) | 1 | NULL allowed | _Indicates whether the transaction is a financial transaction ( eg cashin ) or not ( eg, view bill ).Service_Types created by system has IS_FINANCIAL column as null. User can not do any modification in this. Also for this type of service_types Display_Allowed is set to 'N'. There is only one Service_Type 'SMSBAL' (Balance Enquiry) for which Display_Allowed is 'Y' and Is_Financial is null because it is not fixed (SMSBAL can be defined as Financial or NonFinancial)_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SysServiceTypesv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_SysServiceTypesv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

