#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransferMoneyDaily

# ![Tables](../../../../Images/Table32.png) [in].[TransferMoneyDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TransferMoneyDaily: IDDimDate\WalletID\TransactionKey](../../../../Images/pkcluster.png)](#indexes) | TransactionKey | int | 4 | NOT NULL |
|  | QuantityP | bigint | 8 | NOT NULL |
|  | TotalAmountP | numeric(24,6) | 13 | NOT NULL |
|  | QuantityN | bigint | 8 | NOT NULL |
|  | TotalAmountN | numeric(24,6) | 13 | NOT NULL |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

