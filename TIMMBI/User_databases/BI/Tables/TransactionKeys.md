#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.TransactionKeys

# ![Tables](../../../../Images/Table32.png) [in].[TransactionKeys]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TransactionKeys: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |  |
| [![Indexes IX_TransactionKeys](../../../../Images/Index.png)](#indexes) | Source | varchar(5) | 5 | NOT NULL |  | _Source of the data_ |
| [![Indexes IX_TransactionKeys](../../../../Images/Index.png)](#indexes) | ShortName | varchar(50) | 50 | NULL allowed |  |  |
|  | Description | varchar(200) | 200 | NOT NULL |  |  |
|  | Fee | bit | 1 | NOT NULL | ((0)) |  |
|  | Bonus | bit | 1 | NOT NULL | ((0)) |  |
|  | Recharge | bit | 1 | NOT NULL | ((0)) |  |
|  | Transfer | bit | 1 | NOT NULL | ((0)) |  |
|  | Type | varchar(10) | 10 | NULL allowed |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
|  | IDOrigDest | int | 4 | NULL allowed |  |  |
|  | FeeOM | bit | 1 | NOT NULL | ((0)) |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TransactionKeys: ID](../../../../Images/pkcluster.png)](#indexes) | PK_TransactionKeys | ID | YES | IN |
|  | IX_TransactionKeys | Source, ShortName |  | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[vwt_ConsumptionDistDaily]](../Views/vwt_ConsumptionDistDaily.md)
* [[in].[vwt_ConsumptionDistMonthly]](../Views/vwt_ConsumptionDistMonthly.md)
* [[in].[vwt_SubsConsumptionDistDaily]](../Views/vwt_SubsConsumptionDistDaily.md)
* [[in].[vwt_SubsConsumptionDistMonthly]](../Views/vwt_SubsConsumptionDistMonthly.md)
* [[TIMM_Reports].[dbo].[rpt_RevenuePerSite]](../../TIMM_Reports/Programmability/Stored_Procedures/rpt_RevenuePerSite.md)
* [[External].[dbo].[spc_DecrementalReport]](../../External/Programmability/Stored_Procedures/spc_DecrementalReport.md)
* [[External].[dbo].[spc_DecrementalReportV9]](../../External/Programmability/Stored_Procedures/spc_DecrementalReportV9.md)
* [[in].[spc_GetConsumptionPerSite]](../Programmability/Stored_Procedures/spc_GetConsumptionPerSite.md)
* [[in].[spc_GetGeneralDailyOverview]](../Programmability/Stored_Procedures/spc_GetGeneralDailyOverview.md)
* [[in].[spc_GetRevenueTotalPerSite]](../Programmability/Stored_Procedures/spc_GetRevenueTotalPerSite.md)
* [[in].[spc_GetTransactionsDaily]](../Programmability/Stored_Procedures/spc_GetTransactionsDaily.md)
* [[in].[spc_GetWalletBalanceOverview]](../Programmability/Stored_Procedures/spc_GetWalletBalanceOverview.md)
* [[in].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage.md)
* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

