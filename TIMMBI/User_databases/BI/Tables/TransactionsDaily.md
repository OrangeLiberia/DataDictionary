#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransactionsDaily

# ![Tables](../../../../Images/Table32.png) [in].[TransactionsDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransactionsDaily: IDDimDate\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_TransactionsDaily: IDDimDate\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL | _Transaction Key (see [in.TransactionKeys](TransactionKeys.md))_ |
| [![Cluster Primary Key PK_TransactionsDaily: IDDimDate\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_TransactionsDaily: IDDimDate\TransactionKey\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint | 1 | NOT NULL | _IN ID (see [in.INs](INs.md))_ |
|  | QuantityP | int | 4 | NOT NULL | _Quantity of Positives Transactions_ |
|  | ChargeableAmountP | float | 8 | NOT NULL | _Total Amount of Positives Transactions_ |
|  | QuantityN | int | 4 | NOT NULL | _Quantity of Negatives Transactions_ |
|  | ChargeableAmountN | float | 8 | NOT NULL |  |


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

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

