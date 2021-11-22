#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsCallsPerCellDeviceMonthly1

# ![Tables](../../../../Images/Table32.png) [in].[SubsCallsPerCellDeviceMonthly1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceMonthly1: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceMonthly1: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |  |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceMonthly1: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceMonthly1: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | CellID | int |  | 4 | NOT NULL | _Phone IMEI (imported from msc from aproximated time of CDR)_ |
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceMonthly1: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | IMEI | varchar(20) |  | 20 | NOT NULL |  |
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
| [![Cluster Primary Key PK_SubsCallsPerCellDeviceMonthly1: IDDimDate\MSISDN\WalletID\CellID\IMEI](../../../../Images/pkcluster.png)](#indexes) | PK_SubsCallsPerCellDeviceMonthly1 | IDDimDate, MSISDN, WalletID, CellID, IMEI | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsCallsPerCellDeviceMonthly]](../Views/SubsCallsPerCellDeviceMonthly.md)
* [[in].[vwt_SubsCallsPerCellDeviceMonthly]](../Views/vwt_SubsCallsPerCellDeviceMonthly.md)
* [[in].[spt_LoadSubsCallsPerCellDevice]](../Programmability/Stored_Procedures/spt_LoadSubsCallsPerCellDevice.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

