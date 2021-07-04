#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ScratchCardsDailyStockMonthly

# ![Tables](../../../../Images/Table32.png) [in].[ScratchCardsDailyStockMonthly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsDailyStockMonthly: IDDimDate\CardAmount](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_ScratchCardsDailyStockMonthly: IDDimDate\CardAmount](../../../../Images/pkcluster.png)](#indexes) | CardAmount | numeric(18,6) | 9 | NOT NULL |
|  | NCards | int | 4 | NOT NULL |
|  | TotalAmount | numeric(38,6) | 17 | NOT NULL |
|  | NLoadedCards | int | 4 | NOT NULL |
|  | NUnloadCards | int | 4 | NOT NULL |
|  | AmountLoaded | numeric(38,6) | 17 | NOT NULL |
|  | AmountUnLoaded | numeric(38,6) | 17 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsDailyStockMonthly: IDDimDate\CardAmount](../../../../Images/pkcluster.png)](#indexes) | PK_ScratchCardsDailyStockMonthly | IDDimDate, CardAmount | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_ExtractScratchCardsStock]](../Programmability/Stored_Procedures/spc_ExtractScratchCardsStock.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

