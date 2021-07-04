#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.TrafficPerCell

# ![Tables](../../../../Images/Table32.png) [dbo].[TrafficPerCell]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | Day | datetime | 8 | NOT NULL |
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | IDDest | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | ProductType | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | WalletType | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | CellID | int | 4 | NOT NULL |
|  | NCalls | int | 4 | NOT NULL |
|  | NCallsAttempts | int | 4 | NOT NULL |
|  | NChrgCalls | int | 4 | NOT NULL |
|  | NFreeCalls | int | 4 | NOT NULL |
|  | ChrgdDurSec | int | 4 | NOT NULL |
|  | FreeDurSec | int | 4 | NOT NULL |
|  | Amount | float | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TrafficPerCell: IDDimDate\IDOrig\IDDest\ProductType\WalletType\CellID](../../../../Images/pkcluster.png)](#indexes) | PK_TrafficPerCell | IDDimDate, IDOrig, IDDest, ProductType, WalletType, CellID | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

