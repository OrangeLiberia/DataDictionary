#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CustomerUsageDaily1

# ![Tables](../../../../Images/Table32.png) [in].[CustomerUsageDaily1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily1: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CustomerUsageDaily1: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW1 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW1OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW1OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW1Intl | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW2 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW3 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW3OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW3OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW3Intl | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW4 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW4OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW4OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW4Intl | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW5 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW6 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW6OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW6OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | ChargeableAmountW6Intl | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | 4GOutOfBundle | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RechargeAmountW1 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RechargeAmountW2 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RechargeAmountW3 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RechargeAmountW4 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RechargeAmountW5 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RechargeAmountW6 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountW1P | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountW1N | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountW4P | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountW4N | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountP | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountN | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | 4GBundles | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | OtherTransactionsP | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | OtherTransactionsN | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RemainCreditW1 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RemainCreditW2 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RemainCreditW3 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RemainCreditW4 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RemainCreditW5 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | RemainCreditW6 | decimal(20,5) |  | 13 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | NMOCalls | int |  | 4 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | MOCDurSec | bigint |  | 8 | NOT NULL |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | NSMOC | int |  | 4 | NOT NULL |  |
| [![Indexes IX_BaseView_CUD1
IX_VIEW](../../../../Images/Index.png)](#indexes)(2) | ChargeableAmount | decimal(25,5) | YES | 13 | NULL allowed |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | OtherTransactions | decimal(21,5) | YES | 13 | NULL allowed |  |
| [![Indexes IX_BaseView_CUD1
IX_VIEW](../../../../Images/Index.png)](#indexes)(2) | RechargeAmount | decimal(25,5) | YES | 13 | NULL allowed |  |
| [![Indexes IX_BaseView_CUD1
IX_VIEW](../../../../Images/Index.png)](#indexes)(2) | TransferAmount | decimal(21,5) | YES | 13 | NULL allowed |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountW1 | decimal(21,5) | YES | 13 | NULL allowed |  |
| [![Indexes IX_VIEW](../../../../Images/Index.png)](#indexes) | TransferAmountW4 | decimal(21,5) | YES | 13 | NULL allowed |  |
|  | ChargeableAmountOMWLRD | decimal(20,5) |  | 13 | NOT NULL | ((0)) |
|  | ChargeableAmountOMWUSD | decimal(20,5) |  | 13 | NOT NULL | ((0)) |
|  | ChargeableAmountOM | decimal(21,5) | YES | 13 | NULL allowed |  |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| ChargeableAmount | ((((([ChargeableAmountW1]+[ChargeableAmountW2])+[ChargeableAmountW3])+[ChargeableAmountW4])+[ChargeableAmountW5])+[ChargeableAmountW6]) |
| OtherTransactions | ([OtherTransactionsP]+[OtherTransactionsN]) |
| RechargeAmount | ((((([RechargeAmountW1]+[RechargeAmountW2])+[RechargeAmountW3])+[RechargeAmountW4])+[RechargeAmountW5])+[RechargeAmountW6]) |
| TransferAmount | ([TransferAmountP]+[TransferAmountN]) |
| TransferAmountW1 | ([TransferAmountW1P]+[TransferAmountW1N]) |
| TransferAmountW4 | ([TransferAmountW4P]+[TransferAmountW4N]) |
| ChargeableAmountOM | ([ChargeableAmountOMWLRD]+[ChargeableAmountOMWUSD]) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique | File Group |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily1: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerUsageDaily1 | IDDimDate, MSISDN |  | YES | IN |
|  | IX_BaseView_CUD1 | ChargeableAmount, RechargeAmount, TransferAmount |  |  | IN |
|  | IX_VIEW | IDDimDate | MOCDurSec, NSMOC, RemainCreditW2, ChargeableAmountW1, ChargeableAmountW1OnNet, ChargeableAmountW1OffNet, ChargeableAmountW1Intl, ChargeableAmountW2, ChargeableAmountW3OnNet, ChargeableAmountW3OffNet, ChargeableAmountW3Intl, ChargeableAmountW4, ChargeableAmountW4OnNet, MSISDN, ChargeableAmountW4Intl, ChargeableAmountW5, ChargeableAmountW6, ChargeableAmountW6OnNet, ChargeableAmountW6OffNet, ChargeableAmountW3, 4GOutOfBundle, ChargeableAmount, RechargeAmountW1, RechargeAmountW2, RechargeAmountW3, ChargeableAmountW4OffNet, RechargeAmountW5, RechargeAmountW6, RechargeAmount, TransferAmountW1P, TransferAmountW1N, ChargeableAmountW6Intl, TransferAmountW4P, TransferAmountW4N, TransferAmountW4, TransferAmountP, TransferAmountN, RechargeAmountW4, 4GBundles, OtherTransactionsP, OtherTransactionsN, OtherTransactions, RemainCreditW1, TransferAmountW1, RemainCreditW3, RemainCreditW4, RemainCreditW5, RemainCreditW6, NMOCalls, TransferAmount |  | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[CustomerUsageDaily]](../Views/CustomerUsageDaily_0009.md)
* [[in].[vwt_CustomerUsageDaily]](../Views/vwt_CustomerUsageDaily.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage.md)
* [[in].[spc_UpdateCustomerEndingBalance]](../Programmability/Stored_Procedures/spc_UpdateCustomerEndingBalance.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

