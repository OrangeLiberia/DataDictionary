#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ScratchCardsDaily

# ![Tables](../../../../Images/Table32.png) [in].[ScratchCardsDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_ScratchCardsDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | SCAmount | numeric(24,6) | 13 | NOT NULL |  |
| [![Cluster Primary Key PK_ScratchCardsDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | WithLoadDate | bit | 1 | NOT NULL | ((1)) |
|  | Quantity | bigint | 8 | NOT NULL |  |
|  | TotalAmount | numeric(24,6) | 13 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | PK_ScratchCardsDaily | IDDimDate, SCAmount, WithLoadDate | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_LoadScratchCards]](../Programmability/Stored_Procedures/spc_LoadScratchCards.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

