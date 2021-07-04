#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsCallsPerCellDeviceDaily2

# ![Tables](../../../../Images/Table32.png) [in].[SubsCallsPerCellDeviceDaily2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceDaily2: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceDaily2: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceDaily2: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceDaily2: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceDaily2: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | IMEI | varchar(20) |  | 20 | NOT NULL |
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
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceDaily2: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | PK_SubsCallsPerCellDeviceDaily2 | IDDimDate, MSISDN, WalletID, CellID, IMEI | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsCallsPerCellDeviceDaily]](../Views/SubsCallsPerCellDeviceDaily.md)
* [[in].[spt_LoadSubsCallsPerCellDevice]](../Programmability/Stored_Procedures/spt_LoadSubsCallsPerCellDevice.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

