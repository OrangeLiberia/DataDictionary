#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsPerCellMonthly1

# ![Tables](../../../../Images/Table32.png) [in].[CallsPerCellMonthly1]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsPerCellMonthly1: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_CallsPerCellMonthly1: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_CallsPerCellMonthly1: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_CallsPerCellMonthly1: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_CallsPerCellMonthly1: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |
|  | NMOCharged | bigint |  | 8 | NOT NULL |
|  | NMOFree | bigint |  | 8 | NOT NULL |
|  | NMOAttempt | bigint |  | 8 | NOT NULL |
|  | MOChargedDurSec | bigint |  | 8 | NOT NULL |
|  | MOFreeDurSec | bigint |  | 8 | NOT NULL |
|  | MOAmount | float |  | 8 | NOT NULL |
|  | NSMOCharged | bigint |  | 8 | NOT NULL |
|  | NSMOFree | bigint |  | 8 | NOT NULL |
|  | SMOAmount | float |  | 8 | NOT NULL |
|  | DataAmount | float |  | 8 | NOT NULL |
|  | NSubs | int |  | 4 | NULL allowed |
|  | Amount | float | YES | 8 | NOT NULL |
|  | MODurSec | bigint | YES | 8 | NULL allowed |
|  | NMO | bigint | YES | 8 | NULL allowed |
|  | NSMO | bigint | YES | 8 | NULL allowed |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| Amount | (([DataAmount]+[SMOAmount])+[MOAmount]) |
| MODurSec | ([MOChargedDurSec]+[MOFreeDurSec]) |
| NMO | (([NMOCharged]+[NMOFree])+[NMOAttempt]) |
| NSMO | ([NSMOFree]+[NSMOCharged]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsPerCellMonthly1: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsPerCellMonthly1 | IDDimDate, CellID, IDOrig, IDDest, WalletID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[CallsPerCellMonthly]](../Views/CallsPerCellMonthly.md)
* [[in].[spt_LoadCallsPerCell]](../Programmability/Stored_Procedures/spt_LoadCallsPerCell.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

