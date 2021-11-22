#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.TransferRulesGeneral

# ![Tables](../../../../Images/Table32.png) [dbo].[TransferRulesGeneral]

---

## <a name="#description"></a>MS_Description

Provides the list of general transfer rules.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferRulesGeneralv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_TransferRulesGeneralv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_TransferRulesGeneralv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | TRANSFER_RULE_ID | numeric(10,0) | 9 | NOT NULL | _Unique Identifier of the Transfer rule_ |
|  | SERVICE_NAME | varchar(50) | 50 | NOT NULL | _Name of the service associated with the transfer rule_ |
|  | SERVICE_TYPE | varchar(10) | 10 | NOT NULL | _Type of the service associated with the transfer rule_ |
|  | PAYER_DOMAIN_CODE | varchar(10) | 10 | NOT NULL | _Domain code of the payer (FK to DomainDetails)_ |
|  | PAYEE_DOMAIN_CODE | varchar(10) | 10 | NOT NULL | _Domain code of the payee (FK to DomainDetails)_ |
|  | PAYER_CATEGORY_CODE | varchar(10) | 10 | NULL allowed | _category code of the payer (FK to CategoryDetails)_ |
|  | PAYEE_CATEGORY_CODE | varchar(10) | 10 | NOT NULL | _category code of the payee (FK to CategoryDetails)_ |
|  | PAYMENT_METHOD_TYPE | varchar(20) | 20 | NOT NULL | _Type of payment method(e.g Wallet)_ |
|  | STATUS_ID | varchar(2) | 2 | NOT NULL | _Status of the transfer rule_ |
|  | TRANSFER_TYPE | varchar(10) | 10 | NOT NULL | _Type of transfer_ |
|  | CREATED_BY | varchar(20) | 20 | NOT NULL | _userId of the user creating the transfer rule_ |
|  | GRPH_DOMAIN_CODE | varchar(10) | 10 | NOT NULL | _Geographical domain of user (Fk to GeographyDomain)_ |
|  | PAYER_PAYMENT_TYPE_ID | numeric(2,0) | 5 | NOT NULL | _Payment type id of the payer. Mapping for payment type id can be found in SysPaymentmethod export (Fk to PaymentType)_ |
|  | PAYEE_PAYMENT_TYPE_ID | numeric(2,0) | 5 | NOT NULL | _Payment type id of the payee. Mapping for payment type id can be found in SysPaymentmethod export (Fk to PaymentType)_ |
|  | CREATED_ON | datetime | 8 | NOT NULL | _Creation date_ |
|  | MODIFIED_BY | varchar(30) | 30 | NOT NULL | _Userid of the user modifying transfer rule_ |
|  | BYPASS_ALLOWED | varchar(1) | 1 | NULL allowed | _Flag to identified if bypass of transfer rule is allowed_ |
|  | DIRECT_TRANSFER_ALLOWED | varchar(1) | 1 | NULL allowed | _Flag to identified if direcct transfer of transfer rule is allowed_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferRulesGeneralv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_TransferRulesGeneralv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

