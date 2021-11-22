#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.ServicesChargesDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[ServicesChargesDetails]

---

## <a name="#description"></a>MS_Description

Contains list of Service Charges received for the transactions created on the targeted day.<br />This export contains also a lot of lines where service charge amount is zero (non-charged transactions), as these NULL charges are logged in the database.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_ID | varchar(20) | 20 | NULL allowed | _Id the the transaction concerned by the service charge_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_DATE | datetime | 8 | NULL allowed | _Creation date of the transaction_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | SERVICE_CHARGE_ID | numeric(10,0) | 9 | NULL allowed | _ID of the service charge range applied to the transaction_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_AMOUNT | numeric(17,2) | 9 | NULL allowed | _Amount of the transaction_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_USER_ID | varchar(20) | 20 | NULL allowed | _user_id of the payer of the service charge_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_CATEGORY_CODE | varchar(20) | 20 | NULL allowed | _Category code of the service charges payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_USER_ID | varchar(20) | 20 | NULL allowed | _user_id of the payee of the service charge. Usually always IND03 account (Operator account dedicated for receiving service charges)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_CATEGORY_CODE | varchar(10) | 10 | NULL allowed | _Category code of the service charges payee. When payer is the IND03 account, the value of the category code is "OPT" (instead of the "OCA Account" value as in previous versions)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | SERVICE_CHARGE_AMOUNT | numeric(17,2) | 9 | NULL allowed | _Amount of the service charge_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | SERVICE_TYPE | varchar(10) | 10 | NULL allowed | _Service type of the transaction_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_STATUS | varchar(3) | 3 | NULL allowed | _Status of the transaction. TS (Transaction Successful), TF (Transaction failed)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_SUBTYPE | varchar(10) | 10 | NULL allowed | _Subtype of the transaction. In most case the Transfer_Subtype is the same as the Service_Type (P2PNONREG, RC, P2P, MERCHPAY, P2PCF, RR_RC, O2C, PAYROLL, C2C, PBILLPAY, ONTHEFLY, COUTBYCODE, SUBREG, OPTW, STOCK, CASHIN, CASHOUT, STKTR2OCA, OPTC)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_DOMAIN_CODE | varchar(10) | 10 | NULL allowed | _Domain code of the service charges payer. Generally the service charge payer is a SUBS ( Subscriber Grade)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_GRADE_NAME | varchar(40) | 40 | NULL allowed | _Grade name (and not code) of the wallet used by the commissions payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_MOBILE_GROUP_ROLE | varchar(38) | 38 | NULL allowed | _Mobile group role of the wallet used by the commissions payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_GROUP_ROLE | varchar(35) | 35 | NULL allowed | _Web group role of the commission payer. Only filled when payer is not a Subscriber_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_MSISDN_ACC | varchar(15) | 15 | NULL allowed | _MSISDN of the service charges payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PARENT_PAYER_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the parent user of the service charges payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PARENT_PAYER_USER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the parent user of the service charges payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | OWNER_PAYER_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the owner of the service charges payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | OWNER_PAYER_USER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the owner of the service charges payer_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYER_WALLET_NUMBER | varchar(25) | 25 | NULL allowed | _Number of the wallet where the commission has been debited_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_DOMAIN_CODE | varchar(10) | 10 | NULL allowed | _Domain code of the service charges payee. Will be filled by the Subscriber (or Channel User) information in case of Service Charge Rollback (Transaction ROLLBACK or TXNCORRECT)_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_GRADE_NAME | varchar(40) | 40 | NULL allowed | _Grade name (and not code) of the wallet used by the commissions payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_MOBILE_GROUP_ROLE | varchar(38) | 38 | NULL allowed | _Mobile group role of the wallet used by the commissions payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_GROUP_ROLE | varchar(35) | 35 | NULL allowed | _Web group role of the commissions payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_MSISDN_ACC | varchar(15) | 15 | NULL allowed | _MSISDN of the service charges payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PARENT_PAYEE_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the parent user of the service charges payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PARENT_PAYEE_USER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the parent user of the service charges payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | OWNER_PAYEE_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the owner of the service charges payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | OWNER_PAYEE_USER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the owner of the service charges payee_ |
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | PAYEE_WALLET_NUMBER | varchar(25) | 25 | NULL allowed | _Number of the wallet where the commission has been credited_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|
| [![Cluster Key cci_ServicesChargesDetailsv1: *](../../../../Images/cluster.png)](#indexes) | cci_ServicesChargesDetailsv1 | FileID, ID, RefDate, CurrencyType, TRANSACTION_ID, TRANSACTION_DATE, SERVICE_CHARGE_ID, TRANSACTION_AMOUNT, PAYER_USER_ID, PAYER_CATEGORY_CODE, PAYEE_USER_ID, PAYEE_CATEGORY_CODE, SERVICE_CHARGE_AMOUNT, SERVICE_TYPE, TRANSFER_STATUS, TRANSFER_SUBTYPE, PAYER_DOMAIN_CODE, PAYER_GRADE_NAME, PAYER_MOBILE_GROUP_ROLE, PAYER_GROUP_ROLE, PAYER_MSISDN_ACC, PARENT_PAYER_USER_ID, PARENT_PAYER_USER_MSISDN, OWNER_PAYER_USER_ID, OWNER_PAYER_USER_MSISDN, PAYER_WALLET_NUMBER, PAYEE_DOMAIN_CODE, PAYEE_GRADE_NAME, PAYEE_MOBILE_GROUP_ROLE, PAYEE_GROUP_ROLE, PAYEE_MSISDN_ACC, PARENT_PAYEE_USER_ID, PARENT_PAYEE_USER_MSISDN, OWNER_PAYEE_USER_ID, OWNER_PAYEE_USER_MSISDN, PAYEE_WALLET_NUMBER | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

