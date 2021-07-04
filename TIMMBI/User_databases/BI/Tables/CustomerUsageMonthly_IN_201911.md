#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.CustomerUsageMonthly_IN_201911

# ![Tables](../../../../Images/Table32.png) [fwk].[CustomerUsageMonthly_IN_201911]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| IDDimDate | int | 4 | NULL allowed |
| MSISDN | varchar(32) | 32 | NULL allowed |
| IN.ChargeableAmountW1 | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW1OnNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW1OffNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW1Intl | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW2 | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW3 | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW3OnNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW3OffNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW3Intl | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW4 | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW4OnNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW4OffNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW4Intl | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW5 | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW6 | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW6OnNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW6OffNet | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmountW6Intl | decimal(20,5) | 13 | NULL allowed |
| IN.4GOutOfBundle | decimal(20,5) | 13 | NULL allowed |
| IN.ChargeableAmount | decimal(25,5) | 13 | NULL allowed |
| IN.RechargeAmountW1 | decimal(20,5) | 13 | NULL allowed |
| IN.RechargeAmountW2 | decimal(20,5) | 13 | NULL allowed |
| IN.RechargeAmountW3 | decimal(20,5) | 13 | NULL allowed |
| IN.RechargeAmountW4 | decimal(20,5) | 13 | NULL allowed |
| IN.RechargeAmountW5 | decimal(20,5) | 13 | NULL allowed |
| IN.RechargeAmountW6 | decimal(20,5) | 13 | NULL allowed |
| IN.RechargeAmount | decimal(25,5) | 13 | NULL allowed |
| IN.TransferAmountW1P | decimal(20,5) | 13 | NULL allowed |
| IN.TransferAmountW1N | decimal(20,5) | 13 | NULL allowed |
| IN.TransferAmountW1 | decimal(21,5) | 13 | NULL allowed |
| IN.TransferAmountW4P | decimal(20,5) | 13 | NULL allowed |
| IN.TransferAmountW4N | decimal(20,5) | 13 | NULL allowed |
| IN.TransferAmountW4 | decimal(21,5) | 13 | NULL allowed |
| IN.TransferAmountP | decimal(20,5) | 13 | NULL allowed |
| IN.TransferAmountN | decimal(20,5) | 13 | NULL allowed |
| IN.TransferAmount | decimal(21,5) | 13 | NULL allowed |
| IN.4GBundles | decimal(20,5) | 13 | NULL allowed |
| IN.OtherTransactionsP | decimal(20,5) | 13 | NULL allowed |
| IN.OtherTransactionsN | decimal(20,5) | 13 | NULL allowed |
| IN.OtherTransactions | decimal(21,5) | 13 | NULL allowed |
| IN.RemainCreditW1 | decimal(20,5) | 13 | NULL allowed |
| IN.RemainCreditW2 | decimal(20,5) | 13 | NULL allowed |
| IN.RemainCreditW3 | decimal(20,5) | 13 | NULL allowed |
| IN.RemainCreditW4 | decimal(20,5) | 13 | NULL allowed |
| IN.RemainCreditW5 | decimal(20,5) | 13 | NULL allowed |
| IN.RemainCreditW6 | decimal(20,5) | 13 | NULL allowed |
| IN.NMOCalls | int | 4 | NULL allowed |
| IN.MOCDurSec | bigint | 8 | NULL allowed |
| IN.NSMOC | int | 4 | NULL allowed |
| MSC.MOCalls | int | 4 | NULL allowed |
| MSC.MODurSec | int | 4 | NULL allowed |
| MSC.MOOnNetCalls | int | 4 | NULL allowed |
| MSC.MOOnNetDurSec | int | 4 | NULL allowed |
| MSC.MOOffNetCalls | int | 4 | NULL allowed |
| MSC.MOOffNetDurSec | int | 4 | NULL allowed |
| MSC.MOIntlCalls | int | 4 | NULL allowed |
| MSC.MOIntlDurSec | int | 4 | NULL allowed |
| MSC.MTCalls | int | 4 | NULL allowed |
| MSC.MTDurSec | int | 4 | NULL allowed |
| MSC.MTOnNetCalls | int | 4 | NULL allowed |
| MSC.MTOnNetDurSec | int | 4 | NULL allowed |
| MSC.MTOffNetCalls | int | 4 | NULL allowed |
| MSC.MTOffNetDurSec | int | 4 | NULL allowed |
| MSC.MTIntlCalls | int | 4 | NULL allowed |
| MSC.MTIntlDurSec | int | 4 | NULL allowed |
| MSC.SMO | int | 4 | NULL allowed |
| MSC.SMOOnNet | int | 4 | NULL allowed |
| MSC.SMOOffNet | int | 4 | NULL allowed |
| MSC.SMOIntl | int | 4 | NULL allowed |
| MSC.SMT | int | 4 | NULL allowed |
| MSC.SMTOnNet | int | 4 | NULL allowed |
| MSC.SMTOffNet | int | 4 | NULL allowed |
| MSC.SMTIntl | int | 4 | NULL allowed |
| MSC.USSD | int | 4 | NULL allowed |
| MSC.DataUpMb | numeric(18,6) | 9 | NULL allowed |
| MSC.DataDownMb | numeric(18,6) | 9 | NULL allowed |


---

## <a name="#uses"></a>Uses

* [fwk]


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

