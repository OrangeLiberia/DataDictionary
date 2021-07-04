#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CellReleaseCausesMonthly

# ![Tables](../../../../Images/Table32.png) [msc].[CellReleaseCausesMonthly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CellReleaseCausesMonthly: IDDimDate\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CellReleaseCausesMonthly: IDDimDate\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CellReleaseCausesMonthly: IDDimDate\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | ReleaseCause | smallint |  | 2 | NOT NULL |  |
|  | CallDuration | int |  | 4 | NULL allowed | ((0)) |
|  | NCallsDur | int |  | 4 | NULL allowed | ((0)) |
|  | NCalls0Dur | int |  | 4 | NULL allowed | ((0)) |
|  | NCalls | int | YES | 4 | NULL allowed |  |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| NCalls | ([NCallsDur]+[NCalls0Dur]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CellReleaseCausesMonthly: IDDimDate\CellID\ReleaseCause](../../../../Images/pkcluster.png)](#indexes) | PK_CellReleaseCausesMonthly | IDDimDate, CellID, ReleaseCause | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_LoadCellReleaseCauses]](../Programmability/Stored_Procedures/spc_LoadCellReleaseCauses.md)
* [[msc].[spt_GetCellTrafficMonthly]](../Programmability/Stored_Procedures/spt_GetCellTrafficMonthly.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

