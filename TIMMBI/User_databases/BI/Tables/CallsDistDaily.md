#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsDistDaily

# ![Tables](../../../../Images/Table32.png) [in].[CallsDistDaily]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|---|
| [![ PK_CallsDistDaily ](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) |  | 10 | NOT NULL |  |
| [![ PK_CallsDistDaily ](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |
| [![ PK_CallsDistDaily ](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL |  |
| [![ PK_CallsDistDaily ](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL |  |
| [![ PK_CallsDistDaily ](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |  |
| [![ PK_CallsDistDaily ](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint |  | 1 | NOT NULL |  |
|  | NSubs | bigint |  | 8 | NOT NULL | ((0)) |
|  | NCallAttempts | bigint |  | 8 | NOT NULL | ((0)) |
|  | NSuccFreeCalls | bigint |  | 8 | NOT NULL | ((0)) |
|  | NSuccChrgCalls | bigint |  | 8 | NOT NULL | ((0)) |
|  | RealDurSecFreeCalls | bigint |  | 8 | NOT NULL | ((0)) |
|  | RealDurSecChrgCalls | bigint |  | 8 | NOT NULL | ((0)) |
|  | BillDurSecFreeCalls | bigint |  | 8 | NOT NULL | ((0)) |
|  | BillDurSecChrgCalls | bigint |  | 8 | NOT NULL | ((0)) |
|  | RateBillDur | float |  | 8 | NOT NULL | ((0)) |
|  | RateRealDur | float |  | 8 | NOT NULL | ((0)) |
|  | DurSec0Cost | bigint | YES | 8 | NOT NULL |  |
|  | DurSecBill0Cost | bigint | YES | 8 | NOT NULL |  |
|  | DurSecBillCost | bigint | YES | 8 | NOT NULL |  |
|  | DurSecCost | bigint | YES | 8 | NOT NULL |  |
|  | NCalls0Cost | bigint | YES | 8 | NULL allowed |  |
|  | NCallsCost | bigint | YES | 8 | NOT NULL |  |
|  | RateBill | float | YES | 8 | NOT NULL |  |
|  | RateDur | float | YES | 8 | NOT NULL |  |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

