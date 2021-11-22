#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ScratchCardsTDRMonthly

# ![Tables](../../../../Images/Table32.png) [in].[ScratchCardsTDRMonthly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsTDRMonthly: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_ScratchCardsTDRMonthly: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | SCAmount | numeric(24,6) | 13 | NOT NULL |  | _Scratch Card Amount (value)_ |
| [![Cluster Primary Key PK_ScratchCardsTDRMonthly: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | WithLoadDate | bit | 1 | NOT NULL | ((1)) |  |
|  | Quantity | bigint | 8 | NOT NULL |  |  |
|  | TotalAmount | numeric(24,6) | 13 | NOT NULL |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsTDRMonthly: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | PK_ScratchCardsTDRMonthly | IDDimDate, SCAmount, WithLoadDate | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_GetRechargesMonthly]](../Programmability/Stored_Procedures/spc_GetRechargesMonthly.md)
* [[in].[spt_LoadScratchCardsTDR]](../Programmability/Stored_Procedures/spt_LoadScratchCardsTDR.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

