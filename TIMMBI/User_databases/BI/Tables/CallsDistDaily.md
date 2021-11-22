#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsDistDaily

# ![Tables](../../../../Images/Table32.png) [in].[CallsDistDaily]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) |  | 10 | NOT NULL |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL |  | _ID of the Calling Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL |  | _ID of the Called Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |  | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint |  | 1 | NOT NULL |  | _IN ID (see [in.INs](INs.md))_ |
|  | NSubs | bigint |  | 8 | NOT NULL | ((0)) | _Number of subscribers_ |
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
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_CallsDistDaily | IDDimDate, Type, IDOrig, IDDest, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[vwt_ConsumptionDistDaily]](../Views/vwt_ConsumptionDistDaily.md)
* [[External].[dbo].[spc_DecrementalReport]](../../External/Programmability/Stored_Procedures/spc_DecrementalReport.md)
* [[External].[dbo].[spc_DecrementalReportV9]](../../External/Programmability/Stored_Procedures/spc_DecrementalReportV9.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_GetCallsDailyDetails]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetails.md)
* [[in].[spc_GetCallsDailyDetailsEx]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetailsEx.md)
* [[in].[spc_GetCallsDailyOverview]](../Programmability/Stored_Procedures/spc_GetCallsDailyOverview.md)
* [[in].[spc_GetCallsMonthlyOverview]](../Programmability/Stored_Procedures/spc_GetCallsMonthlyOverview.md)
* [[in].[spc_GetGeneralDailyOverview]](../Programmability/Stored_Procedures/spc_GetGeneralDailyOverview.md)
* [[in].[spc_GetWalletBalanceOverview]](../Programmability/Stored_Procedures/spc_GetWalletBalanceOverview.md)
* [[in].[spt_LoadCallsDist]](../Programmability/Stored_Procedures/spt_LoadCallsDist.md)
* [[msc].[spt_GetINMSCDailyComparison]](../Programmability/Stored_Procedures/spt_GetINMSCDailyComparison.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

