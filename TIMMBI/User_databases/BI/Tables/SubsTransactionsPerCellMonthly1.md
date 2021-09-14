#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsTransactionsPerCellMonthly1

# ![Tables](../../../../Images/Table32.png) [in].[SubsTransactionsPerCellMonthly1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability  | Description |
|---|---|---|---|---|---|---|
| [![ PK_SubsTransactionsPerCellMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL | Date Dimension ( see [fwk.DimDate](DimDate.md) ) |
| [![ PK_SubsTransactionsPerCellMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL | Subscriber Phone Number |
| [![ PK_SubsTransactionsPerCellMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int |  | 4 | NOT NULL | Transaction identification ( see [in.TransactionKeys](TransactionKeys.md) ) |
| [![ PK_SubsTransactionsPerCellMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL | Wallet identification  ( see [in.WalletTypes](WalletTypes.md) ) |
| [![ PK_SubsTransactionsPerCellMonthly1 ](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL | Cellular site identification
|  | QtyP | bigint |  | 8 | NOT NULL | Number of Positive (money added) Transactions |
|  | AmountP | float |  | 8 | NOT NULL | Amount Positive (money added) Transactions |
|  | QtyN | bigint |  | 8 | NOT NULL | Number of Negative (money deducted) Transactions |
|  | AmountN | float |  | 8 | NOT NULL | Amount Negative (money deducted) Transactions |
|  | Amount | float | YES | 8 | NOT NULL | Total amount of transactions |
|  | Qty | bigint | YES | 8 | NULL allowed | Total quanitity of transactions |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| Amount | ([AmountP]+[AmountN]) |
| Qty | ([QtyP]+[QtyN]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly1: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | PK_SubsTransactionsPerCellMonthly1 | IDDimDate, MSISDN, TransactionKey, WalletID, CellID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsTransactionsPerCellMonthly]](../Views/SubsTransactionsPerCellMonthly.md)
* [[in].[vwt_SubsTransactionsPerCellMonthly]](../Views/vwt_SubsTransactionsPerCellMonthly.md)
* [[in].[spt_LoadSubsTransactionsPerCell]](../Programmability/Stored_Procedures/spt_LoadSubsTransactionsPerCell.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

