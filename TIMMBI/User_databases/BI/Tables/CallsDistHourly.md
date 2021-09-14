#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsDistHourly

# ![Tables](../../../../Images/Table32.png) [in].[CallsDistHourly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| File Group | IN |
| Row Count (~) | 8359547 |
| Created | 12:40:32 PM Tuesday, March 18, 2014 |
| Last Modified | 9:41:31 PM Monday, September 28, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) |  | 10 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimHour | tinyint |  | 1 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |  | _Wallet ID References to ( see [fwk.DimDate](DimDate.md) ) _ |
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint |  | 1 | NOT NULL |  |  |
|  | NSubs | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | NCallAttempts | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | NSuccFreeCalls | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | NSuccChrgCalls | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | RealDurSecFreeCalls | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | RealDurSecChrgCalls | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | BillDurSecFreeCalls | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | BillDurSecChrgCalls | bigint |  | 8 | NOT NULL | ((0)) |  |
|  | RateBillDur | float |  | 8 | NOT NULL | ((0)) |  |
|  | RateRealDur | float |  | 8 | NOT NULL | ((0)) |  |
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
| [![Cluster Primary Key PK_CallsDistHourly: IDDimDate\IDDimHour\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_CallsDistHourly | IDDimDate, IDDimHour, Type, IDOrig, IDDest, WalletID, IN | YES | IN |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | SELECT | Reader |
| Grant | SELECT | TIMM\\BU-Marketing |
| Grant | VIEW DEFINITION | TIMM\\BU-Marketing |
| Grant | SELECT | TIMM\\BU-Sales |
| Grant | VIEW DEFINITION | TIMM\\BU-Sales |
| Grant | SELECT | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | SELECT | TIMM\\BU-Finance |
| Grant | VIEW DEFINITION | TIMM\\BU-Finance |
| Grant | SELECT | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | SELECT | TIMM\\BU-MIS-ADD |
| Grant | VIEW DEFINITION | TIMM\\BU-MIS-ADD |
| Grant | SELECT | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | SELECT | TIMM\\BU-OrangeMoney |
| Grant | VIEW DEFINITION | TIMM\\BU-OrangeMoney |
| Grant | SELECT | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | SELECT | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [in].[CallsDistHourly]
(
[Type] [varchar] (10) COLLATE Latin1_General_CI_AS NOT NULL,
[IDDimDate] [int] NOT NULL,
[IDDimHour] [tinyint] NOT NULL,
[IDOrig] [int] NOT NULL,
[IDDest] [int] NOT NULL,
[WalletID] [int] NOT NULL,
[IN] [tinyint] NOT NULL,
[NSubs] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_NSubs] DEFAULT ((0)),
[NCallAttempts] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_NCallAttempts] DEFAULT ((0)),
[NSuccFreeCalls] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_NSuccFreeCalls] DEFAULT ((0)),
[NSuccChrgCalls] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_NSuccChrgCalls] DEFAULT ((0)),
[RealDurSecFreeCalls] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_RealDurSecFreeCalls] DEFAULT ((0)),
[RealDurSecChrgCalls] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_RealDurSecChrgCalls] DEFAULT ((0)),
[BillDurSecFreeCalls] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_BillDurSecFreeCalls] DEFAULT ((0)),
[BillDurSecChrgCalls] [bigint] NOT NULL CONSTRAINT [DEF_CallsDistHourly_BillDurSecChrgCalls] DEFAULT ((0)),
[RateBillDur] [float] NOT NULL CONSTRAINT [DEF_CallsDistHourly_RateBillDur] DEFAULT ((0)),
[RateRealDur] [float] NOT NULL CONSTRAINT [DEF_CallsDistHourly_RateRealDur] DEFAULT ((0)),
[DurSec0Cost] AS ([RealDurSecFreeCalls]),
[DurSecBill0Cost] AS ([BillDurSecFreeCalls]),
[DurSecBillCost] AS ([BillDurSecChrgCalls]),
[DurSecCost] AS ([RealDurSecChrgCalls]),
[NCalls0Cost] AS ([NCallAttempts]+[NSuccFreeCalls]),
[NCallsCost] AS ([NSuccChrgCalls]),
[RateBill] AS ([RateBillDur]),
[RateDur] AS ([RateRealDur])
) ON [IN]
GO
ALTER TABLE [in].[CallsDistHourly] ADD CONSTRAINT [PK_CallsDistHourly] PRIMARY KEY CLUSTERED  ([IDDimDate], [IDDimHour], [Type], [IDOrig], [IDDest], [WalletID], [IN]) ON [IN]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [olib_bu_finance]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [olib_bu_finance]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [olib_bu_marketing]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [olib_bu_marketing]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [olib_bu_mis_add]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [olib_bu_mis_add]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [olib_bu_orangemoney]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [olib_bu_orangemoney]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [olib_bu_sales]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [olib_bu_sales]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [Reader]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [TIMM\\BU-Finance]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [TIMM\\BU-Finance]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [TIMM\\BU-Marketing]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [TIMM\\BU-Marketing]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [TIMM\\BU-MIS-ADD]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [TIMM\\BU-MIS-ADD]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [TIMM\\BU-OrangeMoney]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [TIMM\\BU-OrangeMoney]
GO
GRANT SELECT ON  [in].[CallsDistHourly] TO [TIMM\\BU-Sales]
GO
GRANT VIEW DEFINITION ON  [in].[CallsDistHourly] TO [TIMM\\BU-Sales]
GO
EXEC sp_addextendedproperty N'MS_Description', 'Wallet ID References to ( see [fwk.DimDate](DimDate.md) ) ', 'SCHEMA', N'in', 'TABLE', N'CallsDistHourly', 'COLUMN', N'WalletID'
GO

```


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [fwk].[spc_DeleteBeforeRun]
* [in].[spc_CleanupCallsDistHourly]
* [in].[spc_GetCallsHourly]
* [in].[spt_LoadCallsDistHourly]


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Tuesday, September 14, 2021 4:34:40 PM

