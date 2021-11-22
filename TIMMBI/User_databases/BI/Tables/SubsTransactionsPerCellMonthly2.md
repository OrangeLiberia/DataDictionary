#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsTransactionsPerCellMonthly2

# ![Tables](../../../../Images/Table32.png) [in].[SubsTransactionsPerCellMonthly2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |  |
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int |  | 4 | NOT NULL | _Transaction Key (see [in.TransactionKeys](TransactionKeys.md))_ |
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL | _Phone IMEI (imported from msc from aproximated time of CDR)_ |
|  | QtyP | bigint |  | 8 | NOT NULL | _Quantity of Positives Transactions_ |
|  | AmountP | float |  | 8 | NOT NULL | _Total Amount of Positives Transactions_ |
|  | QtyN | bigint |  | 8 | NOT NULL | _Quantity of Negatives Transactions_ |
|  | AmountN | float |  | 8 | NOT NULL | _Total Amount of Negatives Transactions_ |
|  | Amount | float | YES | 8 | NOT NULL |  |
|  | Qty | bigint | YES | 8 | NULL allowed |  |


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
| [![Cluster Primary Key PK_SubsTransactionsPerCellMonthly2: IDDimDate\MSISDN\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | PK_SubsTransactionsPerCellMonthly2 | IDDimDate, MSISDN, TransactionKey, WalletID, CellID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsTransactionsPerCellMonthly]](../Views/SubsTransactionsPerCellMonthly.md)
* [[in].[spt_LoadSubsTransactionsPerCell]](../Programmability/Stored_Procedures/spt_LoadSubsTransactionsPerCell.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

