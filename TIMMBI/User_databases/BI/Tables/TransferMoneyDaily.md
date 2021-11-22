#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransferMoneyDaily

# ![Tables](../../../../Images/Table32.png) [in].[TransferMoneyDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL | _Transaction Key (see [in.TransactionKeys](TransactionKeys.md))_ |
|  | QuantityP | bigint | 8 | NOT NULL | _Quantity of Positives Transactions_ |
|  | TotalAmountP | numeric(24,6) | 13 | NOT NULL |  |
|  | QuantityN | bigint | 8 | NOT NULL | _Quantity of Negatives Transactions_ |
|  | TotalAmountN | numeric(24,6) | 13 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | PK_TransferMoneyDaily | IDDimDate, WalletID, TransactionKey | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_GetTransferMoneyDaily]](../Programmability/Stored_Procedures/spc_GetTransferMoneyDaily.md)
* [[in].[spt_LoadTransferMoneyDist]](../Programmability/Stored_Procedures/spt_LoadTransferMoneyDist.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

