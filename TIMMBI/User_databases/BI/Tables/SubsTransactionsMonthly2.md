#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsTransactionsMonthly2

# ![Tables](../../../../Images/Table32.png) [in].[SubsTransactionsMonthly2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |
| [![Cluster Primary Key PK_SubsTransactionsMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsTransactionsMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsTransactionsMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsTransactionsMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint | 1 | NOT NULL |
|  | QuantityP | int | 4 | NOT NULL |
|  | ChargeableAmountP | float | 8 | NOT NULL |
|  | QuantityN | int | 4 | NOT NULL |
|  | ChargeableAmountN | float | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_SubsTransactionsMonthly2 | IDDimDate, MSISDN, TransactionKey, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsTransactionsMonthly]](../Views/SubsTransactionsMonthly.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spt_LoadSubsTransactions]](../Programmability/Stored_Procedures/spt_LoadSubsTransactions.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

