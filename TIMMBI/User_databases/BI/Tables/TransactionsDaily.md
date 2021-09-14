#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransactionsDaily

# ![Tables](../../../../Images/Table32.png) [in].[TransactionsDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![ PK_TransactionsDaily ](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | Date Dimension ( see [fwk.DimDate](DimDate.md) ) |
| [![ PK_TransactionsDaily ](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL | Transaction identification ( see [in.TransactionKeys](TransactionKeys.md) ) |
| [![ PK_TransactionsDaily ](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL | Wallet identification  ( see [in.WalletTypes](WalletTypes.md) ) |
| [![ PK_TransactionsDaily ](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint | 1 | NOT NULL |
|  | QuantityP | int | 4 | NOT NULL | Number of Positive (money added) Transactions |
|  | ChargeableAmountP | float | 8 | NOT NULL | Amount Positive (money added) Transactions |
|  | QuantityN | int | 4 | NOT NULL | Number of Negative (money deducted) Transactions |
|  | ChargeableAmountN | float | 8 | NOT NULL | Amount Negative (money deducted) Transactions |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TransactionsDaily: IDDimDate\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_TransactionsDaily | IDDimDate, TransactionKey, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[vwt_ConsumptionDistDaily]](../Views/vwt_ConsumptionDistDaily.md)
* [[External].[dbo].[spc_DecrementalReport]](../../External/Programmability/Stored_Procedures/spc_DecrementalReport.md)
* [[External].[dbo].[spc_DecrementalReportV9]](../../External/Programmability/Stored_Procedures/spc_DecrementalReportV9.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_GetGeneralDailyOverview]](../Programmability/Stored_Procedures/spc_GetGeneralDailyOverview.md)
* [[in].[spc_GetTransactionsDaily]](../Programmability/Stored_Procedures/spc_GetTransactionsDaily.md)
* [[in].[spc_GetWalletBalanceOverview]](../Programmability/Stored_Procedures/spc_GetWalletBalanceOverview.md)
* [[in].[spt_LoadTransactions]](../Programmability/Stored_Procedures/spt_LoadTransactions.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

