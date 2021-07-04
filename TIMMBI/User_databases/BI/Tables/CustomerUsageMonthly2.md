#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CustomerUsageMonthly2

# ![Tables](../../../../Images/Table32.png) [in].[CustomerUsageMonthly2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageMonthly2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CustomerUsageMonthly2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) |  | 32 | NOT NULL |  |
|  | ChargeableAmountW1 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW1OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW1OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW1Intl | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW2 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW3 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW3OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW3OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW3Intl | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW4 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW4OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW4OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW4Intl | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW5 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW6 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW6OnNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW6OffNet | decimal(20,5) |  | 13 | NOT NULL |  |
|  | ChargeableAmountW6Intl | decimal(20,5) |  | 13 | NOT NULL |  |
|  | 4GOutOfBundle | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RechargeAmountW1 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RechargeAmountW2 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RechargeAmountW3 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RechargeAmountW4 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RechargeAmountW5 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RechargeAmountW6 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | TransferAmountW1P | decimal(20,5) |  | 13 | NOT NULL |  |
|  | TransferAmountW1N | decimal(20,5) |  | 13 | NOT NULL |  |
|  | TransferAmountW4P | decimal(20,5) |  | 13 | NOT NULL |  |
|  | TransferAmountW4N | decimal(20,5) |  | 13 | NOT NULL |  |
|  | TransferAmountP | decimal(20,5) |  | 13 | NOT NULL |  |
|  | TransferAmountN | decimal(20,5) |  | 13 | NOT NULL |  |
|  | 4GBundles | decimal(20,5) |  | 13 | NOT NULL |  |
|  | OtherTransactionsP | decimal(20,5) |  | 13 | NOT NULL |  |
|  | OtherTransactionsN | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RemainCreditW1 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RemainCreditW2 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RemainCreditW3 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RemainCreditW4 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RemainCreditW5 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | RemainCreditW6 | decimal(20,5) |  | 13 | NOT NULL |  |
|  | NMOCalls | int |  | 4 | NOT NULL |  |
|  | MOCDurSec | bigint |  | 8 | NOT NULL |  |
|  | NSMOC | int |  | 4 | NOT NULL |  |
|  | ChargeableAmount | decimal(25,5) | YES | 13 | NULL allowed |  |
|  | OtherTransactions | decimal(21,5) | YES | 13 | NULL allowed |  |
|  | RechargeAmount | decimal(25,5) | YES | 13 | NULL allowed |  |
|  | TransferAmount | decimal(21,5) | YES | 13 | NULL allowed |  |
|  | TransferAmountW1 | decimal(21,5) | YES | 13 | NULL allowed |  |
|  | TransferAmountW4 | decimal(21,5) | YES | 13 | NULL allowed |  |
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

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageMonthly2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerUsageMonthly2 | IDDimDate, MSISDN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[CustomerUsageMonthly]](../Views/CustomerUsageMonthly_000a.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

