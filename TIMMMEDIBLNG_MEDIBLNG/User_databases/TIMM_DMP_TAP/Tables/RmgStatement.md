#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.RmgStatement

# ![Tables](../../../../Images/Table32.png) [dbo].[RmgStatement]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| PartnerTransactingEntity | nvarchar(512) | 1024 | NULL allowed |
| PartnerName | nvarchar(512) | 1024 | NULL allowed |
| ServiceType | nvarchar(512) | 1024 | NULL allowed |
| SettlementType | nvarchar(512) | 1024 | NULL allowed |
| TrafficDirection | nvarchar(512) | 1024 | NULL allowed |
| InvoicePeriod | nvarchar(512) | 1024 | NULL allowed |
| ReceivableCurrency | nvarchar(512) | 1024 | NULL allowed |
| ReceivableCurrencyPeggedRate | decimal(38,8) | 17 | NULL allowed |
| PayableCurrency | nvarchar(512) | 1024 | NULL allowed |
| PayableCurrencyPeggedRate | decimal(38,8) | 17 | NULL allowed |
| ReceivableSource | nvarchar(512) | 1024 | NULL allowed |
| ReceivableTotalSDR | decimal(38,8) | 17 | NULL allowed |
| ReceivableAdjustments | decimal(38,8) | 17 | NULL allowed |
| PostAdjustmentReceivableTotalSDR | decimal(38,8) | 17 | NULL allowed |
| ReceivableTotalCcy | decimal(38,8) | 17 | NULL allowed |
| PayableSource | nvarchar(512) | 1024 | NULL allowed |
| PayableTotalSDR | decimal(38,8) | 17 | NULL allowed |
| PayableAdjustments | decimal(38,8) | 17 | NULL allowed |
| PostAdjustmentPayableTotalSDR | decimal(38,8) | 17 | NULL allowed |
| PayableTotalCcy | decimal(38,8) | 17 | NULL allowed |
| NetDirection | nvarchar(512) | 1024 | NULL allowed |
| NetAmountSDR | decimal(38,8) | 17 | NULL allowed |
| NetAmountSettlementCurrencySC | decimal(38,8) | 17 | NULL allowed |
| OutstandingAmountSC | decimal(38,8) | 17 | NULL allowed |
| USDRate | decimal(38,8) | 17 | NULL allowed |
| NetAmountUSD | decimal(38,8) | 17 | NULL allowed |
| invoiceperiodbegin | datetime | 8 | NULL allowed |
| invoiceperiodend | datetime | 8 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

