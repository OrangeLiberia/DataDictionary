#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.BalanceChannelUsers

# ![Tables](../../../../Images/Table32.png) [dbo].[BalanceChannelUsers]

---

## <a name="#description"></a>MS_Description

Daily summary per channels users and merchant users : Daily summary per user (total number and amount of transactions per type, beginning and ending balance...) Exports this summary only for users who  perform at least one transaction on the given day

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
| [![Cluster Primary Key PK_BalanceChannelUsersv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_BalanceChannelUsersv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_BalanceChannelUsersv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | CATEGORIE | varchar(20) | 20 | NULL allowed | _Category code of the user._ |
|  | PARTY_ID | varchar(20) | 20 | NULL allowed | _User_id of the User_ |
|  | WALLET_NUMBER | varchar(25) | 25 | NULL allowed | _Identifier of the user's wallet used for the transactions_ |
|  | MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN_ |
|  | PARENT_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the User's parent_ |
|  | PARENT_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the User's parent_ |
|  | OWNER_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the User's owner_ |
|  | OWNER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the User's owner_ |
|  | OPENING_BALANCE | numeric(17,2) | 9 | NULL allowed | _Balance of the User at the beginning of the period targetted by the export_ |
|  | CLOSING_BALANCE | numeric(17,2) | 9 | NULL allowed | _Balance of the User at the end of the period targetted by the export_ |
|  | AMT_TRANS_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of all financial transactions (i.e : transfer status = TS) whose financial movements was debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_TRANS_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of all financial transactions (i.e : transfer status = TS) whose financial movements was debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_TRANS_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of all financial transactions (i.e : transfer status = TS) whose financial movements was credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_TRANS_IN | numeric(19,0) | 9 | NULL allowed | _Total number of all financial transactions (i.e : transfer status = TS) whose financial movements was credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_TRANS_REIMB_OUT | numeric(17,2) | 9 | NULL allowed | _Total number of Commissions debited from the wallet (to IND03). Exception : doesnt include the transactions correction (service type = TXNCORRECT or ROLLBACK)._ |
|  | NB_TRANS_REIMB_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions debited from the wallet (to IND03). Exception : doesnt include the transactions correction (service type = TXNCORRECT or ROLLBACK)._ |
|  | AMT_TRANS_REIMB_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions credited to the wallet (from IND03). Exception : doesnt include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_TRANS_REIMB_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions credited to the wallet (from IND03). Exception : doesnt include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_SC_OUT | numeric(17,2) | 9 | NULL allowed | _Total number of  Service Charges debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_SC_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of  Service Charges debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_SC_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of  Service Charges Paid (or Reimbursed) credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_SC_IN | numeric(19,0) | 9 | NULL allowed | _Total number of  Service Charges Paid (or Reimbursed) credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions debited from the wallet (to IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions debited from the wallet (to IND03). Exception : doesn't include the transactions correction (service type = 'TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions credited to the wallet (from IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_IN | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions credited to the wallet (from IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_REIMB_OUT | numeric(17,2) | 9 | NULL allowed | _Total number of Commissions Reimbursed debited from the wallet (to IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_REIMB_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions Reimbursed debited from the wallet (to IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_REIMB_IN | numeric(17,2) | 9 | NULL allowed | _Total number of Commissions reimbursed credited to the wallet (from IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_REIMB_IN | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions reimbursed credited to the wallet (from IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_OUT_OTHER | numeric(17,2) | 9 | NULL allowed | _Total number of Commissions credited to the wallet (from Other Source). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_OUT_OTHER | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions credited to the wallet (from Other Source). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_IN_OTHER | numeric(17,2) | 9 | NULL allowed | _Total number of Commissions Reimbursed debited from the wallet (to Other Payee) (Service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_IN_OTHER | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions Reimbursed debited from the wallet (to Other Payee)<br />( Service type = TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_REIMB_OUT_OTHER | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions reimbursed credited to the wallet (from Other Source)<br />(Service type = 'TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_REIMB_OUT_OTHER | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions reimbursed credited to the wallet (from Other Source)<br />( Service type = 'TXNCORRECT or ROLLBACK)_ |
|  | AMT_COM_REIMB_IN_OTHER | numeric(17,2) | 9 | NULL allowed | _Total number of Commissions reimbursed credited to the wallet (from Other Source)<br />(i.e. : Service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_COM_REIMB_IN_OTHER | numeric(19,0) | 9 | NULL allowed | _Total number of Commissions reimbursed credited to the wallet (from Other Source)<br />(Service type = TXNCORRECT or ROLLBACK)_ |
|  | NB_NONFIN_TRANS | numeric(19,0) | 9 | NULL allowed | _Total number of non-financial Transactions executed on the Wallet_ |
|  | NB_NONFIN_TRANS_CANCELLED | numeric(19,0) | 9 | NULL allowed | _Total number of non-financial Transactions cancelled on the Wallet_ |
|  | AMT_SC_NONFIN_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Service Charges on Non-Financial Trx debited from the wallet_ |
|  | NB_SC_NONFIN_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of Service Charges on Non-Financial Trx debited from the wallet_ |
|  | AMT_SC_NONFIN_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of  Service Charges on Non-Financial Trx credited to the wallet_ |
|  | NB_SC_NONFIN_IN | numeric(19,0) | 9 | NULL allowed | _Total number of  Service Charges on Non-Financial Trx credited to the wallet_ |
|  | AMT_COM_NONFIN_OUT | numeric(17,2) | 9 | NULL allowed | _Total number of Commission on Non-Financial Trx debited from the wallet_ |
|  | NB_COM_NONFIN_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of  Commission on Non-Financial Trx credited to the wallet_ |
|  | AMT_COM_NONFIN_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of  Commission on Non-Financial Trx credited to the wallet_ |
|  | NB_COM_NONFIN_IN | numeric(19,0) | 9 | NULL allowed | _Total number of  Commission on Non-Financial Trx credited to the wallet_ |
|  | AMT_TOTAL_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Debit movements from the Wallet (including rollback, reimbursement, service charge, commissions, etc. )_ |
|  | NB_TOTAL_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of Debit movements from the Wallet (including rollback, reimbursement, service charge, commissions, etc. )_ |
|  | AMT_TOTAL_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of Credit movements to the Wallet  (including rollback, reimbursement, service charge, commissions, etc. )_ |
|  | NB_TOTAL_IN | numeric(19,0) | 9 | NULL allowed | _Total number of Credit movements to the Wallet (including rollback, reimbursement, service charge, commissions, etc. )_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_BalanceChannelUsersv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_BalanceChannelUsersv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

