#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ScratchCardsTDRDaily

# ![Tables](../../../../Images/Table32.png) [in].[ScratchCardsTDRDaily]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsTDRDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_ScratchCardsTDRDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | SCAmount | numeric(24,6) | 13 | NOT NULL |  |
| [![Cluster Primary Key PK_ScratchCardsTDRDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | WithLoadDate | bit | 1 | NOT NULL | ((1)) |
|  | Quantity | bigint | 8 | NOT NULL |  |
|  | TotalAmount | numeric(24,6) | 13 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsTDRDaily: IDDimDate\SCAmount\WithLoadDate](../../../../Images/pkcluster.png)](#indexes) | PK_ScratchCardsTDRDaily | IDDimDate, SCAmount, WithLoadDate | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_GetRechargesDaily]](../Programmability/Stored_Procedures/spc_GetRechargesDaily.md)
* [[in].[spt_LoadScratchCardsTDR]](../Programmability/Stored_Procedures/spt_LoadScratchCardsTDR.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

