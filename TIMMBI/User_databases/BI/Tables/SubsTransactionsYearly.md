#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsTransactionsYearly

# ![Tables](../../../../Images/Table32.png) [in].[SubsTransactionsYearly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsYearly: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |  |
| [![Cluster Primary Key PK_SubsTransactionsYearly: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_SubsTransactionsYearly: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL | _Transaction Key (see [in.TransactionKeys](TransactionKeys.md))_ |
| [![Cluster Primary Key PK_SubsTransactionsYearly: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_SubsTransactionsYearly: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint | 1 | NOT NULL | _IN ID (see [in.INs](INs.md))_ |
|  | QuantityP | int | 4 | NOT NULL | _Quantity of Positives Transactions_ |
|  | ChargeableAmountP | float | 8 | NOT NULL | _Total Amount of Positives Transactions_ |
|  | QuantityN | int | 4 | NOT NULL | _Quantity of Negatives Transactions_ |
|  | ChargeableAmountN | float | 8 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsYearly: IDDimDate\MSISDN\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_SubsTransactionsYearly | IDDimDate, MSISDN, TransactionKey, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spt_LoadSubsTransactions]](../Programmability/Stored_Procedures/spt_LoadSubsTransactions.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

