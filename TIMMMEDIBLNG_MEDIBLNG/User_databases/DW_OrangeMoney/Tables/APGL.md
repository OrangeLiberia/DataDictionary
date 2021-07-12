#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.APGL

# ![Tables](../../../../Images/Table32.png) [dbo].[APGL]

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
| [![Cluster Primary Key PK_APGLv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_APGLv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_APGLv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
|  | CurrencyType | varchar(16) | 16 | NOT NULL |
|  | SENDER_MSISDN | varchar(60) | 60 | NOT NULL |
|  | RECEIVER_MSISDN | varchar(60) | 60 | NOT NULL |
|  | SENDER_USER_ID | varchar(20) | 20 | NOT NULL |
|  | RECEIVER_USER_ID | varchar(20) | 20 | NOT NULL |
|  | SERVICE_TYPE | varchar(10) | 10 | NOT NULL |
|  | TRANSFER_SUBTYPE | varchar(10) | 10 | NOT NULL |
|  | SENDER_COUNTRY_CODE | varchar(2) | 2 | NOT NULL |
|  | RECEIVER_COUNTRY_CODE | varchar(2) | 2 | NOT NULL |
|  | TRANSACTION_STATUS | varchar(3) | 3 | NOT NULL |
|  | SENDER_PRE_BALANCE | numeric(17,2) | 9 | NOT NULL |
|  | SENDER_POST_BALANCE | numeric(17,2) | 9 | NOT NULL |
|  | RECEIVER_PRE_BALANCE | numeric(17,2) | 9 | NOT NULL |
|  | RECEIVER_POST_BALANCE | numeric(17,2) | 9 | NOT NULL |
|  | REFERENCE_NUMBER | varchar(255) | 255 | NOT NULL |
|  | REMARKS | varchar(150) | 150 | NOT NULL |
|  | TRANSACTION_ID | varchar(20) | 20 | NOT NULL |
|  | TRANSACTION_DATE_TIME | datetime | 8 | NOT NULL |
|  | SENDER_CATEGORY_CODE | varchar(20) | 20 | NOT NULL |
|  | RECEIVER_CATEGORY_CODE | varchar(20) | 20 | NOT NULL |
|  | SENDER_DOMAIN_CODE | varchar(10) | 10 | NOT NULL |
|  | RECEIVER_DOMAIN_CODE | varchar(10) | 10 | NOT NULL |
|  | SENDER_DESIGNATION | varchar(30) | 30 | NOT NULL |
|  | RECEIVER_DESIGNATION | varchar(30) | 30 | NOT NULL |
|  | SENDER_STATE | varchar(60) | 60 | NOT NULL |
|  | RECEIVER_STATE | varchar(60) | 60 | NOT NULL |
|  | TRANSACTION_AMOUNT | numeric(17,2) | 9 | NOT NULL |
|  | COMMISSION_GROSSISTE | numeric(17,2) | 9 | NOT NULL |
|  | COMMISSION_AGENT | numeric(17,2) | 9 | NOT NULL |
|  | COMMISSION_OCA | numeric(17,2) | 9 | NOT NULL |
|  | COMMISSION_AUTRE | numeric(17,2) | 9 | NOT NULL |
|  | SERVICE_CHARGE_AMOUNT | numeric(17,2) | 9 | NOT NULL |
|  | TRANSACTION_TAG | varchar(50) | 50 | NOT NULL |
|  | IS_FINANCIAL | varchar(1) | 1 | NOT NULL |
|  | ZEBRA | varchar(10) | 10 | NOT NULL |
|  | ROLLBACKED | varchar(1) | 1 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_APGLv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_APGLv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

