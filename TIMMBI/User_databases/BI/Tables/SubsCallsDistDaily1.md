#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsCallsDistDaily1

# ![Tables](../../../../Images/Table32.png) [in].[SubsCallsDistDaily1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |  |  |
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) |  | 10 | NOT NULL |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL |  | _ID of the Calling Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL |  | _ID of the Called Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |  | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint |  | 1 | NOT NULL |  | _IN ID (see [in.INs](INs.md))_ |
|  | NCallAttempts | bigint |  | 8 | NOT NULL | ((0)) | _Number of attempted calls_ |
|  | NSuccFreeCalls | bigint |  | 8 | NOT NULL | ((0)) | _Number of success free calls_ |
|  | NSuccChrgCalls | bigint |  | 8 | NOT NULL | ((0)) | _Number of sucess charged calls_ |
|  | RealDurSecFreeCalls | bigint |  | 8 | NOT NULL | ((0)) | _Real duration of free calls_ |
|  | RealDurSecChrgCalls | bigint |  | 8 | NOT NULL | ((0)) | _Real duration of charged calls_ |
|  | BillDurSecFreeCalls | bigint |  | 8 | NOT NULL | ((0)) | _Rounded duration of free calls_ |
|  | BillDurSecChrgCalls | bigint |  | 8 | NOT NULL | ((0)) | _Rounded duration of charged calls_ |
|  | RateBillDur | float |  | 8 | NOT NULL | ((0)) | _Rate of Rounded duration_ |
|  | RateRealDur | float |  | 8 | NOT NULL | ((0)) | _Rate of Real duration_ |
|  | DurSec0Cost | bigint | YES | 8 | NOT NULL |  |  |
|  | DurSecBill0Cost | bigint | YES | 8 | NOT NULL |  |  |
|  | DurSecBillCost | bigint | YES | 8 | NOT NULL |  |  |
|  | DurSecCost | bigint | YES | 8 | NOT NULL |  |  |
|  | NCalls0Cost | bigint | YES | 8 | NULL allowed |  |  |
|  | NCallsCost | bigint | YES | 8 | NOT NULL |  |  |
|  | RateBill | float | YES | 8 | NOT NULL |  |  |
|  | RateDur | float | YES | 8 | NOT NULL |  |  |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| DurSec0Cost | ([RealDurSecFreeCalls]) |
| DurSecBill0Cost | ([BillDurSecFreeCalls]) |
| DurSecBillCost | ([BillDurSecChrgCalls]) |
| DurSecCost | ([RealDurSecChrgCalls]) |
| NCalls0Cost | ([NCallAttempts]+[NSuccFreeCalls]) |
| NCallsCost | ([NSuccChrgCalls]) |
| RateBill | ([RateBillDur]) |
| RateDur | ([RateRealDur]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsDistDaily1: IDDimDate\MSISDN\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_SubsCallsDistDaily1 | IDDimDate, MSISDN, Type, IDOrig, IDDest, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsCallsDistDaily]](../Views/SubsCallsDistDaily.md)
* [[in].[vwt_SubsCallsDistDaily]](../Views/vwt_SubsCallsDistDaily.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[_spt_LoadSubsCallsDist_CB]](../Programmability/Stored_Procedures/_spt_LoadSubsCallsDist_CB.md)
* [[in].[spt_LoadSubsCallsDist]](../Programmability/Stored_Procedures/spt_LoadSubsCallsDist.md)
* [[in].[spt_LoadSubsCallsDist_Aux]](../Programmability/Stored_Procedures/spt_LoadSubsCallsDist_Aux.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

