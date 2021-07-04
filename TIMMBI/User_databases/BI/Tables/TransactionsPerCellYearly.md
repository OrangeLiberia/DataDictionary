#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransactionsPerCellYearly

# ![Tables](../../../../Images/Table32.png) [in].[TransactionsPerCellYearly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransactionsPerCellYearly: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransactionsPerCellYearly: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransactionsPerCellYearly: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransactionsPerCellYearly: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL |
|  | QtyP | bigint |  | 8 | NOT NULL |
|  | AmountP | float |  | 8 | NOT NULL |
|  | QtyN | bigint |  | 8 | NOT NULL |
|  | AmountN | float |  | 8 | NOT NULL |
|  | NSubs | int |  | 4 | NULL allowed |
|  | Amount | float | YES | 8 | NOT NULL |
|  | Qty | bigint | YES | 8 | NULL allowed |


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
| [![Cluster Primary Key PK_TransactionsPerCellYearly: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | PK_TransactionsPerCellYearly | IDDimDate, TransactionKey, WalletID, CellID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[spt_LoadTransactionsPerCell]](../Programmability/Stored_Procedures/spt_LoadTransactionsPerCell.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

