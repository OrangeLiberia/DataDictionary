#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsDistYearly

# ![Tables](../../../../Images/Table32.png) [in].[CallsDistYearly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) |  | 10 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IDDest | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | WalletID | int |  | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | IN | tinyint |  | 1 | NOT NULL |  |
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
| [![Cluster Primary Key PK_CallsDistYearly: IDDimDate\Type\IDOrig\IDDest\WalletID\IN](../../../../Images/pkcluster.png)](#indexes) | PK_CallsDistYearly | IDDimDate, Type, IDOrig, IDDest, WalletID, IN | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spt_LoadCallsDist]](../Programmability/Stored_Procedures/spt_LoadCallsDist.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

