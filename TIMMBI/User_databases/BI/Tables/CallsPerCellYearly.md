#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsPerCellYearly

# ![Tables](../../../../Images/Table32.png) [in].[CallsPerCellYearly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsPerCellYearly: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_CallsPerCellYearly: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL | _Phone IMEI (imported from msc from aproximated time of CDR)_ |
| [![Cluster Primary Key PK_CallsPerCellYearly: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL | _ID of the Calling Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_CallsPerCellYearly: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL | _ID of the Called Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_CallsPerCellYearly: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
|  | NMOCharged | bigint |  | 8 | NOT NULL | _Number of MO charged calls_ |
|  | NMOFree | bigint |  | 8 | NOT NULL | _Number of MO free calls_ |
|  | NMOAttempt | bigint |  | 8 | NOT NULL | _Number of MO attempts calls_ |
|  | MOChargedDurSec | bigint |  | 8 | NOT NULL | _Duration of charged calls_ |
|  | MOFreeDurSec | bigint |  | 8 | NOT NULL | _Duration of free calls_ |
|  | MOAmount | float |  | 8 | NOT NULL | _Amount charged on MO calls_ |
|  | NSMOCharged | bigint |  | 8 | NOT NULL | _Number of MO charged sms_ |
|  | NSMOFree | bigint |  | 8 | NOT NULL | _Number of MO free sms_ |
|  | SMOAmount | float |  | 8 | NOT NULL | _Amount charged on MO sms_ |
|  | DataAmount | float |  | 8 | NOT NULL | _Amount charged on data_ |
|  | NSubs | int |  | 4 | NULL allowed | _Number of subscribers_ |
|  | Amount | float | YES | 8 | NOT NULL |  |
|  | MODurSec | bigint | YES | 8 | NULL allowed | _Duration of MO calls_ |
|  | NMO | bigint | YES | 8 | NULL allowed |  |
|  | NSMO | bigint | YES | 8 | NULL allowed |  |


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
| [![Cluster Primary Key PK_CallsPerCellYearly: IDDimDate\CellID\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsPerCellYearly | IDDimDate, CellID, IDOrig, IDDest, WalletID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[spt_LoadCallsPerCell]](../Programmability/Stored_Procedures/spt_LoadCallsPerCell.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

