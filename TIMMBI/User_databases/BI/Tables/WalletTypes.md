#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.WalletTypes

# ![Tables](../../../../Images/Table32.png) [in].[WalletTypes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_WalletTypes: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |
|  | ShortName | varchar(20) | 20 | NOT NULL |  |
|  | Name | varchar(50) | 50 | NOT NULL |  |
|  | BI | varchar(3) | 3 | NULL allowed |  |
|  | Main | bit | 1 | NULL allowed |  |
|  | Bonus | bit | 1 | NULL allowed | ((0)) |
|  | Extra | bit | 1 | NULL allowed | ((0)) |
|  | Currency | varchar(5) | 5 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_WalletTypes: ID](../../../../Images/pkcluster.png)](#indexes) | PK_WalletTypes | ID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[BIDMP_CONSUMPTION_EXPORT]](../../External/Programmability/Stored_Procedures/BIDMP_CONSUMPTION_EXPORT.md)
* [[External].[dbo].[spc_DecrementalReport]](../../External/Programmability/Stored_Procedures/spc_DecrementalReport.md)
* [[External].[dbo].[spc_DecrementalReportV9]](../../External/Programmability/Stored_Procedures/spc_DecrementalReportV9.md)
* [[External].[dbo].[spc_LoadLDvsUSDReport]](../../External/Programmability/Stored_Procedures/spc_LoadLDvsUSDReport.md)
* [[in].[spc_GetARPUDistMonthlyDetails]](../Programmability/Stored_Procedures/spc_GetARPUDistMonthlyDetails.md)
* [[in].[spc_GetCallsDailyDetails]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetails.md)
* [[in].[spc_GetCallsDailyDetailsEx]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetailsEx.md)
* [[in].[spc_GetCallsDailyDetailsExB2B]](../Programmability/Stored_Procedures/spc_GetCallsDailyDetailsExB2B.md)
* [[in].[spc_GetCallsDailyOverview]](../Programmability/Stored_Procedures/spc_GetCallsDailyOverview.md)
* [[in].[spc_GetConsumptionDailyOverview]](../Programmability/Stored_Procedures/spc_GetConsumptionDailyOverview.md)
* [[in].[spc_GetConsumptionMonthlyOverview]](../Programmability/Stored_Procedures/spc_GetConsumptionMonthlyOverview.md)
* [[in].[spc_GetGeneralDailyOverview]](../Programmability/Stored_Procedures/spc_GetGeneralDailyOverview.md)
* [[in].[spc_GetTransactionsDaily]](../Programmability/Stored_Procedures/spc_GetTransactionsDaily.md)
* [[in].[spc_GetTransferMoneyDaily]](../Programmability/Stored_Procedures/spc_GetTransferMoneyDaily.md)
* [[in].[spc_GetWalletBalanceOverview]](../Programmability/Stored_Procedures/spc_GetWalletBalanceOverview.md)
* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

