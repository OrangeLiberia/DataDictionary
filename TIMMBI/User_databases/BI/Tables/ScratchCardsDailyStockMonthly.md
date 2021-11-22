#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ScratchCardsDailyStockMonthly

# ![Tables](../../../../Images/Table32.png) [in].[ScratchCardsDailyStockMonthly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsDailyStockMonthly: IDDimDate\CardAmount](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_ScratchCardsDailyStockMonthly: IDDimDate\CardAmount](../../../../Images/pkcluster.png)](#indexes) | CardAmount | numeric(18,6) | 9 | NOT NULL |  |
|  | NCards | int | 4 | NOT NULL |  |
|  | TotalAmount | numeric(38,6) | 17 | NOT NULL |  |
|  | NLoadedCards | int | 4 | NOT NULL |  |
|  | NUnloadCards | int | 4 | NOT NULL |  |
|  | AmountLoaded | numeric(38,6) | 17 | NOT NULL |  |
|  | AmountUnLoaded | numeric(38,6) | 17 | NOT NULL |  |


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

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

