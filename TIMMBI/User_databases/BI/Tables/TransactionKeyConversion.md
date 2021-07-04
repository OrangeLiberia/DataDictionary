#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransactionKeyConversion

# ![Tables](../../../../Images/Table32.png) [in].[TransactionKeyConversion]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Indexes IX_TransactionKeyConversion](../../../../Images/Index.png)](#indexes) | Accumulator | int | 4 | NOT NULL |
| [![Indexes IX_TransactionKeyConversion](../../../../Images/Index.png)](#indexes) | ProductID | int | 4 | NULL allowed |
|  | TransactionKey | int | 4 | NOT NULL |
|  | Obs | varchar(500) | 500 | NULL allowed |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

