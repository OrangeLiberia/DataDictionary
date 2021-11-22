#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CustomerUsageDaily2

# ![Tables](../../../../Images/Table32.png) [in].[CustomerUsageDaily2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |  |  |
|  | ChargeableAmountW1 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 1_ |
|  | ChargeableAmountW1OnNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 1 on Onnet_ |
|  | ChargeableAmountW1OffNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 1 on OffNet_ |
|  | ChargeableAmountW1Intl | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 1 on International_ |
|  | ChargeableAmountW2 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 2_ |
|  | ChargeableAmountW3 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 3_ |
|  | ChargeableAmountW3OnNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 3 on Onnet_ |
|  | ChargeableAmountW3OffNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 3 on OffNet_ |
|  | ChargeableAmountW3Intl | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 3 on International_ |
|  | ChargeableAmountW4 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 4_ |
|  | ChargeableAmountW4OnNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 4 on Onnet_ |
|  | ChargeableAmountW4OffNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 4 on OffNet_ |
|  | ChargeableAmountW4Intl | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 4 on International_ |
|  | ChargeableAmountW5 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 5_ |
|  | ChargeableAmountW6 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 6_ |
|  | ChargeableAmountW6OnNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 6 on Onnet_ |
|  | ChargeableAmountW6OffNet | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 6 on OffNet_ |
|  | ChargeableAmountW6Intl | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on Wallet 6 on International_ |
|  | 4GOutOfBundle | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on data PAYGO_ |
|  | RechargeAmountW1 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount recharged on Wallet 1_ |
|  | RechargeAmountW2 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount recharged on Wallet 2_ |
|  | RechargeAmountW3 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount recharged on Wallet 3_ |
|  | RechargeAmountW4 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount recharged on Wallet 4_ |
|  | RechargeAmountW5 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount recharged on Wallet 5_ |
|  | RechargeAmountW6 | decimal(20,5) |  | 13 | NOT NULL |  | _Amount recharged on Wallet 6_ |
|  | TransferAmountW1P | decimal(20,5) |  | 13 | NOT NULL |  | _Amount transfered on Wallet 1 Positive_ |
|  | TransferAmountW1N | decimal(20,5) |  | 13 | NOT NULL |  | _Amount transfered on Wallet 1 Negative_ |
|  | TransferAmountW4P | decimal(20,5) |  | 13 | NOT NULL |  | _Amount transfered on Wallet 4 Positive_ |
|  | TransferAmountW4N | decimal(20,5) |  | 13 | NOT NULL |  | _Amount transfered on Wallet 4 Negative_ |
|  | TransferAmountP | decimal(20,5) |  | 13 | NOT NULL |  | _Amount transfered Positive_ |
|  | TransferAmountN | decimal(20,5) |  | 13 | NOT NULL |  | _Amount transfered Negative_ |
|  | 4GBundles | decimal(20,5) |  | 13 | NOT NULL |  | _Amount charged on data bundles_ |
|  | OtherTransactionsP | decimal(20,5) |  | 13 | NOT NULL |  | _Amount on other transactions Positive_ |
|  | OtherTransactionsN | decimal(20,5) |  | 13 | NOT NULL |  | _Amount on other transactions Negative_ |
|  | RemainCreditW1 | decimal(20,5) |  | 13 | NOT NULL |  | _Remain credit on Wallet 1_ |
|  | RemainCreditW2 | decimal(20,5) |  | 13 | NOT NULL |  | _Remain credit on Wallet 2_ |
|  | RemainCreditW3 | decimal(20,5) |  | 13 | NOT NULL |  | _Remain credit on Wallet 3_ |
|  | RemainCreditW4 | decimal(20,5) |  | 13 | NOT NULL |  | _Remain credit on Wallet 4_ |
|  | RemainCreditW5 | decimal(20,5) |  | 13 | NOT NULL |  | _Remain credit on Wallet 5_ |
|  | RemainCreditW6 | decimal(20,5) |  | 13 | NOT NULL |  | _Remain credit on Wallet 6_ |
|  | NMOCalls | int |  | 4 | NOT NULL |  | _Number of MO calls_ |
|  | MOCDurSec | bigint |  | 8 | NOT NULL |  | _Duration of MO calls_ |
|  | NSMOC | int |  | 4 | NOT NULL |  | _Number of MO sms_ |
| [![Indexes IX_BaseView_CUD2](../../../../Images/Index.png)](#indexes) | ChargeableAmount | decimal(25,5) | YES | 13 | NULL allowed |  |  |
|  | OtherTransactions | decimal(21,5) | YES | 13 | NULL allowed |  |  |
| [![Indexes IX_BaseView_CUD2](../../../../Images/Index.png)](#indexes) | RechargeAmount | decimal(25,5) | YES | 13 | NULL allowed |  |  |
| [![Indexes IX_BaseView_CUD2](../../../../Images/Index.png)](#indexes) | TransferAmount | decimal(21,5) | YES | 13 | NULL allowed |  |  |
|  | TransferAmountW1 | decimal(21,5) | YES | 13 | NULL allowed |  |  |
|  | TransferAmountW4 | decimal(21,5) | YES | 13 | NULL allowed |  |  |
|  | ChargeableAmountOMWLRD | decimal(20,5) |  | 13 | NOT NULL | ((0)) |  |
|  | ChargeableAmountOMWUSD | decimal(20,5) |  | 13 | NOT NULL | ((0)) |  |
|  | ChargeableAmountOM | decimal(21,5) | YES | 13 | NULL allowed |  |  |


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

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerUsageDaily2 | IDDimDate, MSISDN | YES | IN |
|  | IX_BaseView_CUD2 | ChargeableAmount, RechargeAmount, TransferAmount |  | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[CustomerUsageDaily]](../Views/CustomerUsageDaily_0009.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage.md)
* [[in].[spc_UpdateCustomerEndingBalance]](../Programmability/Stored_Procedures/spc_UpdateCustomerEndingBalance.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

