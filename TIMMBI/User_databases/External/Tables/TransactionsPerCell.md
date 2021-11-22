#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.TransactionsPerCell

# ![Tables](../../../../Images/Table32.png) [dbo].[TransactionsPerCell]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TransactionsPerCell: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | Day | datetime | 8 | NOT NULL |
| [![Cluster Primary Key PK_TransactionsPerCell: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransactionsPerCell: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransactionsPerCell: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | CellID | int | 4 | NOT NULL |
|  | Qty | int | 4 | NOT NULL |
|  | Amount | float | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TransactionsPerCell: IDDimDate\TransactionKey\WalletID\CellID](../../../../Images/pkcluster.png)](#indexes) | PK_TransactionsPerCell | IDDimDate, TransactionKey, WalletID, CellID | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

