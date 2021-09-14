#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsTransactionsMonthly1

# ![Tables](../../../../Images/Table32.png) [in].[SubsTransactionsMonthly1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![ PK_SubsTransactionsMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL | Subscriber Phone Number |
| [![ PK_SubsTransactionsMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  Date Dimension ( see [fwk.DimDate](DimDate.md) ) |
| [![ PK_SubsTransactionsMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL | Transaction identification ( see [in.TransactionKeys](TransactionKeys.md) ) |
| [![ PK_SubsTransactionsMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL | Wallet identification  ( see [in.WalletTypes](WalletTypes.md) ) |
| [![ PK_SubsTransactionsMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint | 1 | NOT NULL |
|  | QuantityP | int | 4 | NOT NULL  | Number of Positive (money added) Transactions |
|  | ChargeableAmountP | float | 8 | NOT NULL | Amount Positive (money added) Transactions |
|  | QuantityN | int | 4 | NOT NULL | Number of Negative (money deducted) Transactions |
|  | ChargeableAmountN | float | 8 | NOT NULL | Amount Negative (money deducted) Transactions |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsMonthly1: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_SubsTransactionsMonthly1 | IDDimDate, MSISDN, TransactionKey, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsTransactionsMonthly]](../Views/SubsTransactionsMonthly.md)
* [[in].[vwt_SubsTransactionsMonthly]](../Views/vwt_SubsTransactionsMonthly.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spt_LoadSubsTransactions]](../Programmability/Stored_Procedures/spt_LoadSubsTransactions.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

