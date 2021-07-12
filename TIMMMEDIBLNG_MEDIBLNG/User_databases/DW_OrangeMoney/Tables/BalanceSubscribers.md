#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.BalanceSubscribers

# ![Tables](../../../../Images/Table32.png) [dbo].[BalanceSubscribers]

---

## <a name="#description"></a>MS_Description

Daily summary per subscriber (total number and amount of transactions per type, beginning and ending balance...) Exports this summary only for Subscribers who  perform at least one transaction on the given day

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
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | CATEGORIE | varchar(20) | 20 | NULL allowed | _Category code of the user._ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | PARTY_ID | varchar(20) | 20 | NULL allowed | _User_id of the User_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | WALLET_NUMBER | varchar(25) | 25 | NULL allowed | _Identifier of the user's wallet used for the transactions_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the User_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | PARENT_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the User's parent_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | PARENT_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the User's parent _ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | OWNER_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the User's owner_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | OWNER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the User's owner_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | OPENING_BALANCE | numeric(17,2) | 9 | NULL allowed | _Balance of the User at the beginning of the period_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | CLOSING_BALANCE | numeric(17,2) | 9 | NULL allowed | _Balance of the User at the end of the period_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_TRANS_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of all financial transactions (i.e : transfer status = TS) whose financial movements was debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_TRANS_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of all financial transactions (i.e : transfer status = TS) whose financial movements was debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_TRANS_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of all financial transactions (i.e : transfer status = TS) whose financial movements was credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_TRANS_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of all financial transactions (i.e : transfer status = TS) whose financial movements was credited to the wallet.Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_TRANS_REIMB_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of all transactions corrections (i.e. : service type = TXNCORRECT or ROLLBACK) debited from the Wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_TRANS_REIMB_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of all transactions corrections (i.e. : service type = TXNCORRECT or ROLLBACK) debited from the Wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_TRANS_REIMB_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of all transactions corrections (i.e. : service type = TXNCORRECT or ROLLBACK) credited to the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_TRANS_REIMB_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of all transactions corrections (i.e. : service type = TXNCORRECT or ROLLBACK) credited to the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_SC_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Service Charges debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_SC_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of Service Charges debited from the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_SC_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of  Service Charges Paid (or Reimbursed) credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_SC_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of  Service Charges Paid (or Reimbursed) credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions debited from the wallet (to IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions debited from the wallet (to IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of  Service Charges Paid (or Reimbursed) credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of  Service Charges Paid (or Reimbursed) credited to the wallet. Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_REIMB_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions Reimbursed debited from the wallet (to IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_REIMB_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions Reimbursed debited from the wallet (to IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_REIMB_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions reimbursed credited to the wallet (from IND03) (Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_REIMB_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions reimbursed credited to the wallet (from IND03) ( Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_OUT_OTHER | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions debited from the wallet (to Other than IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_OUT_OTHER | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions debited from the wallet (to Other than IND03). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_IN_OTHER | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions credited to the wallet (from Other Source). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_IN_OTHER | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions credited to the wallet (from Other Source). Exception : doesn't include the transactions correction (service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_REIMB_OUT_OTHER | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions Reimbursed debited from the wallet (to Other Payee)<br />(i.e. : Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_REIMB_OUT_OTHER | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions Reimbursed debited from the wallet (to Other Payee)<br />(i.e. : Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_REIMB_IN_OTHER | numeric(17,2) | 9 | NULL allowed | _Total amount of Commissions reimbursed credited to the wallet (from Other Source)<br />(i.e. : Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_REIMB_IN_OTHER | numeric(19,0) | 9 | NULL allowed | _Total amount of Commissions reimbursed credited to the wallet (from Other Source)<br />(i.e. : Service type = TXNCORRECT or ROLLBACK)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_NONFIN_TRANS | numeric(19,0) | 9 | NULL allowed | _Total number of non-financial Transactions executed on the Wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_NONFIN_TRANS_CANCELLED | numeric(19,0) | 9 | NULL allowed | _Total number of non-financial Transactions cancelled on the Wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_SC_NONFIN_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Service Charges on Non-Financial Trx debited from the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_SC_NONFIN_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of Service Charges on Non-Financial Trx debited from the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_SC_NONFIN_IN | numeric(17,2) | 9 | NULL allowed | _Total amount of  Service Charges on Non-Financial Trx credited to the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_SC_NONFIN_IN | numeric(19,0) | 9 | NULL allowed | _Total amount of  Service Charges on Non-Financial Trx credited to the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_NONFIN_OUT | numeric(17,2) | 9 | NULL allowed | _Total amount of Commission on Non-Financial Trx debited from the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_NONFIN_OUT | numeric(19,0) | 9 | NULL allowed | _Total amount of Commission on Non-Financial Trx debited from the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_COM_NONFIN_IN | numeric(17,2) | 9 | NULL allowed | _Total number of  Commission on Non-Financial Trx credited to the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_COM_NONFIN_IN | numeric(19,0) | 9 | NULL allowed | _Total number of  Commission on Non-Financial Trx credited to the wallet_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_OUT | numeric(17,2) | 9 | NULL allowed | _Total number of Debit movements from the Wallet (including rollback, reimbursement, service charge, commissions, etc. …)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_OUT | numeric(19,0) | 9 | NULL allowed | _Total number of Debit movements from the Wallet (including rollback, reimbursement, service charge, commissions, etc. …)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | AMT_IN | numeric(17,2) | 9 | NULL allowed | _Total number of Credit movements to the Wallet (including rollback, reimbursement, service charge, commissions, etc. …)_ |
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | NB_IN | numeric(19,0) | 9 | NULL allowed | _Total number of Credit movements to the Wallet (including rollback, reimbursement, service charge, commissions, etc. …)_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|
| [![Cluster Key cci_BalanceSubscribersv1: *](../../../../Images/cluster.png)](#indexes) | cci_BalanceSubscribersv1 | FileID, ID, RefDate, CurrencyType, CATEGORIE, PARTY_ID, WALLET_NUMBER, MSISDN, PARENT_USER_ID, PARENT_MSISDN, OWNER_USER_ID, OWNER_MSISDN, OPENING_BALANCE, CLOSING_BALANCE, AMT_TRANS_OUT, NB_TRANS_OUT, AMT_TRANS_IN, NB_TRANS_IN, AMT_TRANS_REIMB_OUT, NB_TRANS_REIMB_OUT, AMT_TRANS_REIMB_IN, NB_TRANS_REIMB_IN, AMT_SC_OUT, NB_SC_OUT, AMT_SC_IN, NB_SC_IN, AMT_COM_OUT, NB_COM_OUT, AMT_COM_IN, NB_COM_IN, AMT_COM_REIMB_OUT, NB_COM_REIMB_OUT, AMT_COM_REIMB_IN, NB_COM_REIMB_IN, AMT_COM_OUT_OTHER, NB_COM_OUT_OTHER, AMT_COM_IN_OTHER, NB_COM_IN_OTHER, AMT_COM_REIMB_OUT_OTHER, NB_COM_REIMB_OUT_OTHER, AMT_COM_REIMB_IN_OTHER, NB_COM_REIMB_IN_OTHER, NB_NONFIN_TRANS, NB_NONFIN_TRANS_CANCELLED, AMT_SC_NONFIN_OUT, NB_SC_NONFIN_OUT, AMT_SC_NONFIN_IN, NB_SC_NONFIN_IN, AMT_COM_NONFIN_OUT, NB_COM_NONFIN_OUT, AMT_COM_NONFIN_IN, NB_COM_NONFIN_IN, AMT_OUT, NB_OUT, AMT_IN, NB_IN | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

