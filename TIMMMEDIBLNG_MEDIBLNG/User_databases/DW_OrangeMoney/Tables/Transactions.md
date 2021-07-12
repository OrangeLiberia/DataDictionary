#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.Transactions

# ![Tables](../../../../Images/Table32.png) [dbo].[Transactions]

---

## <a name="#description"></a>MS_Description

Contains new and updated transactions (tag ACTION_TYPE indicates if the transaction is a new one, or an update of a pasted one).

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
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_MSISDN | varchar(15) | 15 | NOT NULL | _MSISDN of the sender of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_MSISDN | varchar(15) | 15 | NOT NULL | _MSISDN of the receiver of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_USER_ID | varchar(20) | 20 | NOT NULL | _User ID of the receiver of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_USER_ID | varchar(20) | 20 | NOT NULL | _User ID if the sender of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_AMOUNT | numeric(17,2) | 9 | NOT NULL | _Transaction amount_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | COMMISSIONS_PAID | numeric(17,2) | 9 | NOT NULL | _Total amount of commissions paid by Orange Money for this transaction (maybe splitted in multiple commissions received by several different users)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | COMMISSIONS_RECEIVED | numeric(17,2) | 9 | NOT NULL | _Total amount of commissions received by Orange Money (in IND03) for this transaction. It can be the sum of multiple commissions received from several different users. (Ex: reimbursement of paid commissions in case of a transaction rollback)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | COMMISSIONS_OTHERS | numeric(17,2) | 9 | NOT NULL | _Total amount of commissions where Orange Money IND03 account is not implied (ex: commission paid by PTUPS account to the subscriber)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SERVICE_CHARGE_RECEIVED | numeric(17,2) | 9 | NOT NULL | _Total amount of service charges  received by Orange Money for this transaction. It can be the sum of multiple commissions received from several different users._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SERVICE_CHARGE_PAID | numeric(17,2) | 9 | NOT NULL | _Service charges reimbursed by Orange Money to subscriber when rollback or transaction correction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TAXES | numeric(17,2) | 9 | NOT NULL | _Total amount of taxes received for this transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SERVICE_TYPE | varchar(10) | 10 | NOT NULL | _Service type of the transaction:. P2PNONREG, RC, P2P, MERCHPAY, O2C, PAYROLL, BILLPAY, COUTBYCODE, OTF, OPTW, STOCK, CASHIN, CASHOUT, STKTR2OCA, OPTC, etc._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_STATUS | varchar(3) | 3 | NOT NULL | _Status of the transaction. TF (Transaction Failed), TS (Transaction Successful), TPI (Transaction Initiated for P2P), TI (Transaction Initiated)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_PRE_BAL | numeric(17,2) | 9 | NOT NULL | _Balance of the sender before the transaction _ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_POST_BAL | numeric(17,2) | 9 | NOT NULL | _Balance of the sender after the transaction (taking into account the transaction amount, service charges and commissions)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_PRE_BAL | numeric(17,2) | 9 | NOT NULL | _Balance of the receiver before the transaction _ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_POST_BAL | numeric(17,2) | 9 | NOT NULL | _Balance of the receiver after the transaction (taking into account the transaction amount, service charges and commissions)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_ACC_STATUS | varchar(2) | 2 | NULL allowed | _Current status of the sender at the time of the data export (maybe modified between the transaction time and the export time)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_ACC_STATUS | varchar(2) | 2 | NULL allowed | _Current status of the receiver at the time of the data export (maybe modified between the transaction time and the export time)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ERROR_CODE | varchar(20) | 20 | NULL allowed | _When transaction is failed, code of the error encountered_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ERROR_DESC | varchar(350) | 350 | NULL allowed | _Description corresponding to the above error code_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | REFERENCE_NUMBER | varchar(100) | 100 | NULL allowed | _Refer to:<br />- the TRANSFER_ID of an other transaction link with (example : transaction for reimbursment, rollback, correction, P2P, etc ...)<br />- the MSISDN of an Operator Withdraw<br />- a value filled manually by on operator. Outputs the value of the first field found filled in the following order RECONCILISATION_BY, RECONCILISATION_FOR, EXT_TXN_NUMBER, ORIGINAL_REF_NUMBER_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | CREATED_ON | datetime | 8 | NOT NULL | _Creation date of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | CREATED_BY | varchar(20) | 20 | NOT NULL | _user_id of the use that initialize the transaction. value SYSTEM when transaction initialized by an Orange Money batch (for example for P2P or RC reimbursments) _ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | MODIFIED_ON | datetime | 8 | NOT NULL | _Date of the transaction update (for example when confirmation of a cashout, OPTW, STOCK, O2C..., or when modification of the reference_number field when completion of a P2P on-the-fly with a SUBREG...). Same value than in created_on if the transaction has not be modified_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | MODIFIED_BY | varchar(20) | 20 | NOT NULL | _user_id of the user that is source of the update (for example user who confirms the transaction in case of cashout, OPTW, STOCK, O2C...., or user who registers the new subscriber in case of P2P on-the-fly...). Same value than in created_by if the transaction has not been modified_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | APP_1_DATE | datetime | 8 | NULL allowed | _Date of the first level of approval for the transaction (generally for O2C and STOCK)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | APP_2_DATE | datetime | 8 | NULL allowed | _Date of the second/last level of approval for the transaction (generally for O2C, STOCK and OPTW)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_ID | varchar(20) | 20 | NOT NULL | _Unique ID of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_DATETIME | datetime | 8 | NOT NULL | _Date of the transaction (usually contains the same value than in created_on)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_CATEGORY_CODE | varchar(10) | 10 | NULL allowed | _Category code of the sender_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_DOMAIN_CODE | varchar(10) | 10 | NULL allowed | _Domain code of the sender_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_GRADE_NAME | varchar(40) | 40 | NULL allowed | _Name (and not code) of the grade of the sender _ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_GROUP_ROLE | varchar(35) | 35 | NULL allowed | _Group_role assigned to the sender (not filled when the receiver is not a Channel User)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_DESIGNATION | varchar(30) | 30 | NULL allowed | _Value of the designation field of the sender (not filled when the sender is not a Channel User). This field can be used to categorize some special Channel Users._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_STATE | varchar(30) | 30 | NULL allowed | _Value of the state field of the sender (not filled when the sender is not a Subscriber). This field can be used to categorize some special Subscribers._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_CATEGORY_CODE | varchar(10) | 10 | NULL allowed | _Category code of the receiver_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_DOMAIN_CODE | varchar(10) | 10 | NULL allowed | _Domain code of the receiver_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_GRADE_NAME | varchar(40) | 40 | NULL allowed | _Name (and not code) of the grade of the receiver _ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_GROUP_ROLE | varchar(35) | 35 | NULL allowed | _Group_role assigned to the receiver (not filled when the receiver is not a Channel User). List of possible values available at Channel User registration_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_DESIGNATION | varchar(30) | 30 | NULL allowed | _Value of the designation field of the receiver (not filled when the receiver is not a Channel User). This field can be used to categorize some special Channel Users._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_STATE | varchar(30) | 30 | NULL allowed | _Value of the state field of the receiver (not filled when the receiver is not a Subscriber). This field can be used to categorize some special Subscribers._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_CITY | varchar(30) | 30 | NULL allowed | _City of the sender_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_CITY | varchar(30) | 30 | NULL allowed | _City of the receiver_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | APP_1_BY | varchar(30) | 30 | NULL allowed | _user_id of the Orange Money user who has validated the transaction at the first level of approval_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | APP_2_BY | varchar(30) | 30 | NULL allowed | _user_id of the Orange Money user who has validated the transaction at the second/last level of approval_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | REQUEST_SOURCE | varchar(10) | 10 | NULL allowed | _source of the transaction request. seems to always contain the value BROWSER_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | GATEWAY_TYPE | varchar(10) | 10 | NULL allowed | _gateway type of the transaction request. USSD, WEB_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_SUBTYPE | varchar(10) | 10 | NULL allowed | _Subtype of the transaction (gives more precision than the service_type alone). P2PNONREG, RC, P2P, MERCHPAY, P2PCF, RR_RC, O2C, PAYROLL, C2C, PBILLPAY, ONTHEFLY, COUTBYCODE, SUBREG, OPTW, STOCK, CASHIN, CASHOUT, STKTR2OCA, OPTC (and maybe more)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | PAYMENT_TYPE | varchar(255) | 255 | NULL allowed | _Payment type for O2C transactions (otherwise empty). Others, Cheque, Cash, Demand Draft (and maybe others, depending in the country ?)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | PAYMENT_NUMBER | varchar(255) | 255 | NULL allowed | _Payment number for O2C transactions (otherwise empty)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | PAYMENT_DATE | datetime | 8 | NULL allowed | _Payment date for O2C transactions (otherwise empty)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | REMARKS | varchar(100) | 100 | NULL allowed | _Remarks (can be filled in the web interface for O2C transactions, otherwise empty)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ACTION_TYPE | varchar(20) | 20 | NULL allowed | _This field indicates wether the transaction is logged because of its creation, approbation or modification. Indeed, this field contains the value CREATION, APPROBATION, or MODIFICATION according to the following rules:<br />- value CREATION when the logged transaction is a new one (transaction initialized the day targetted by the data extraction)<br />- value APPROBATION when the transaction has already been logged when created (on a previous day), but has been approved (at first or second level) on the day targetted by the data extraction.<br />- value MODIFICATION when the transaction has already been logged when created (on a previous day), but has been modified on the day targetted by the data extraction.<br />This MODIFICATION type usually happens for P2P on-the-fly transactions, when the on-the-fly transaction is updated to fill the reference_number field (filled with the transaction ID of the linked SUBREG - for transfer to the new user -  or P2PCF - for reimbursment - transaction)<br /><br />
Notes:<br />- When using this data file to calculate total number or amount of transactions of the day, DO NOT COUNT modified transactions (as they have been already count on their creation day).<br />- For transactions that have been approved on a different day from their creation, be careful to count them only ONCE (either at creation or at approval)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_TAG | varchar(50) | 50 | NOT NULL | _Tag enabling to identify more precisely the transaction type depending on the service type, and on the characteristics of the sender and the receiver._ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECONCILIATION_BY | varchar(20) | 20 | NULL allowed | _Indicates the TRANSFER_ID of the roolback or transaction correction (TXNCORRECT) used to reimburse this transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECONCILIATION_FOR | varchar(50) | 50 | NULL allowed | _Reciprocally to RECONCILIATION_BY,  indicates the TRANSFER_ID of the initial transaction corrected by this rollback or transaction correction (TXNCORRECT). In case of transaction correction (TXNCORRECT) can be filled manualy_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | EXT_TXN_NUMBER | varchar(50) | 50 | NULL allowed | _This field is a TRANSFER_ID value that can be used to link an external transactions. Currently used by most countries for rechage transaction (TOPUP)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ORIGINAL_REF_NUMBER | varchar(100) | 100 | NULL allowed | _Value provided by Tango as the original reference number for another transaction linked with like TRANSFER_ID of P2P, MSISDN of Operator Withdraw. Can be filled manually in the Tango Web interface for some  specific transaction like O2C, OPTW_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ZEBRA_AMBIGUOUS | varchar(10) | 10 | NULL allowed | _Response of Zebra server for RC transaction when ambiguous at zebra side (still waiting for a Zebra final status, or if TF the final Zebra status was Failed after being Ambiguous). <br />Used in case of RC only. If the RC is TS and the ZEBRA_AMBIGUOUS value is AM, then it means that Zebra has not yet validated the top-up : it can become TF, if the final Zebra answer if Failed_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | ATTEMPT_STATUS | varchar(20) | 20 | NULL allowed | _In case of identical transaction (when a user initiates a transaction similar to a previous one in a short period of time), Tango askes him to confirm or cancel this duplicated transaction. This field contains the answer of the user (or No Response if he didn't answer to Tango). (Request cancelled, Request Confirmed, No Response)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | OTHER_MSISDN | varchar(255) | 255 | NULL allowed | _When another user is implied in the transaction (for example, in case of top up for others), msisdn of this other user_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_WALLET_NUMBER | varchar(25) | 25 | NULL allowed | _Identifier of the wallet used by the sender of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_WALLET_NUMBER | varchar(25) | 25 | NULL allowed | _Identifier of the wallet used by the receiver of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_USER_NAME | varchar(80) | 80 | NULL allowed | _user name of the sender of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_USER_NAME | varchar(80) | 80 | NULL allowed | _user name of the receiver of the transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TNO_MSIDN | varchar(15) | 15 | NULL allowed | _MSISDN  of the receiver specified when intiating a TNO (P2PNONREG)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TNO_ID | varchar(30) | 30 | NULL allowed | _ID number of the receiver specified when intiating a TNO (P2PNONREG) (ref. RECEIVER KYC -> P2P_TRANSFER_ID)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | UNREG_FIRST_NAME | varchar(80) | 80 | NULL allowed | _First name of the non orange user who withdraws the COUTBYCODE (ref. RECEIVER KYC -> REC_FNAME)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | UNREG_LAST_NAME | varchar(80) | 80 | NULL allowed | _Last name of the non orange user who withdraws the COUTBYCODE (ref. RECEIVER KYC -> REC_LNAME)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | UNREG_DOB | datetime | 8 | NULL allowed | _Date of Birth of the non orange user who withdraws the COUTBYCODE (ref. RECEIVER KYC -> REC_DOB)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | UNREG_ID_NUMBER | varchar(15) | 15 | NULL allowed | _ID Number of the non orange user who withdraws the COUTBYCODE (ref. RECEIVER KYC -> REC_IDNO)_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | BULK_PAYOUT_BATCHID | varchar(255) | 255 | NULL allowed | _ID of the batch in case of bulk transaction_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | IS_FINANCIAL | varchar(1) | 1 | NULL allowed | _Indicates whether the transaction is a financial one or not. Indeed, in this report, all financial transactions will be traced, but also non financial ones that have service charges applied_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | TRANSFER_DONE | varchar(1) | 1 | NULL allowed | _Indicates if the UV transfer has been realized between Orange Money accounts or not. Indeed, some transactions are logged as TF whereas the transfer has been done (e.g. when transactions are rollbaked).  _ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | INITIATOR_MSISDN | varchar(16) | 16 | NULL allowed | _New field for transactions corrections_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | VALIDATOR_MSISDN | varchar(16) | 16 | NULL allowed | _New field for transactions corrections_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | INITIATOR_COMMENTS | varchar(96) | 96 | NULL allowed | _New field for transactions corrections_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | VALIDATOR_COMMENTS | varchar(96) | 96 | NULL allowed | _New field for transactions corrections_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_WALLET_NAME | varchar(64) | 64 | NULL allowed | _New field for multi-wallet_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_WALLET_NAME | varchar(64) | 64 | NULL allowed | _New field for multi-wallet_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | SENDER_USER_TYPE | varchar(64) | 64 | NULL allowed | _New field for multi-wallet_ |
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | RECEIVER_USER_TYPE | varchar(64) | 64 | NULL allowed | _New field for multi-wallet_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|
| [![Cluster Key cci_TransactionsEx: *](../../../../Images/cluster.png)](#indexes) | cci_TransactionsEx | FileID, ID, RefDate, CurrencyType, SENDER_MSISDN, RECEIVER_MSISDN, RECEIVER_USER_ID, SENDER_USER_ID, TRANSACTION_AMOUNT, COMMISSIONS_PAID, COMMISSIONS_RECEIVED, COMMISSIONS_OTHERS, SERVICE_CHARGE_RECEIVED, SERVICE_CHARGE_PAID, TAXES, SERVICE_TYPE, TRANSFER_STATUS, SENDER_PRE_BAL, SENDER_POST_BAL, RECEIVER_PRE_BAL, RECEIVER_POST_BAL, SENDER_ACC_STATUS, RECEIVER_ACC_STATUS, ERROR_CODE, ERROR_DESC, REFERENCE_NUMBER, CREATED_ON, CREATED_BY, MODIFIED_ON, MODIFIED_BY, APP_1_DATE, APP_2_DATE, TRANSFER_ID, TRANSFER_DATETIME, SENDER_CATEGORY_CODE, SENDER_DOMAIN_CODE, SENDER_GRADE_NAME, SENDER_GROUP_ROLE, SENDER_DESIGNATION, SENDER_STATE, RECEIVER_CATEGORY_CODE, RECEIVER_DOMAIN_CODE, RECEIVER_GRADE_NAME, RECEIVER_GROUP_ROLE, RECEIVER_DESIGNATION, RECEIVER_STATE, SENDER_CITY, RECEIVER_CITY, APP_1_BY, APP_2_BY, REQUEST_SOURCE, GATEWAY_TYPE, TRANSFER_SUBTYPE, PAYMENT_TYPE, PAYMENT_NUMBER, PAYMENT_DATE, REMARKS, ACTION_TYPE, TRANSACTION_TAG, RECONCILIATION_BY, RECONCILIATION_FOR, EXT_TXN_NUMBER, ORIGINAL_REF_NUMBER, ZEBRA_AMBIGUOUS, ATTEMPT_STATUS, OTHER_MSISDN, SENDER_WALLET_NUMBER, RECEIVER_WALLET_NUMBER, SENDER_USER_NAME, RECEIVER_USER_NAME, TNO_MSIDN, TNO_ID, UNREG_FIRST_NAME, UNREG_LAST_NAME, UNREG_DOB, UNREG_ID_NUMBER, BULK_PAYOUT_BATCHID, IS_FINANCIAL, TRANSFER_DONE, INITIATOR_MSISDN, VALIDATOR_MSISDN, INITIATOR_COMMENTS, VALIDATOR_COMMENTS, SENDER_WALLET_NAME, RECEIVER_WALLET_NAME, SENDER_USER_TYPE, RECEIVER_USER_TYPE | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

