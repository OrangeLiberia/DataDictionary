#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransactionKeyConversion

# ![Tables](../../../../Images/Table32.png) [in].[TransactionKeyConversion]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Indexes IX_TransactionKeyConversion](../../../../Images/Index.png)](#indexes) | Accumulator | int | 4 | NOT NULL |  |
| [![Indexes IX_TransactionKeyConversion](../../../../Images/Index.png)](#indexes) | ProductID | int | 4 | NULL allowed |  |
|  | TransactionKey | int | 4 | NOT NULL | _Transaction Key (see [in.TransactionKeys](TransactionKeys.md))_ |
|  | Obs | varchar(500) | 500 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns | File Group |
|---|---|---|
| IX_TransactionKeyConversion | Accumulator, ProductID | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[spc_TransformationTransactionsDaily]](../Programmability/Stored_Procedures/spc_TransformationTransactionsDaily.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

