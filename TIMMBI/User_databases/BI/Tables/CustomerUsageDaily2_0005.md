#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CustomerUsageDaily2

# ![Tables](../../../../Images/Table32.png) [msc].[CustomerUsageDaily2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_CustomerUsageDaily2](../../../../Images/Index.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_CustomerUsageDaily2](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |
|  | IDOrigDest | int | 4 | NOT NULL |
|  | MOCalls | int | 4 | NOT NULL |
|  | MODurSec | int | 4 | NOT NULL |
|  | MOOnNetCalls | int | 4 | NOT NULL |
|  | MOOnNetDurSec | int | 4 | NOT NULL |
|  | MOOffNetCalls | int | 4 | NOT NULL |
|  | MOOffNetDurSec | int | 4 | NOT NULL |
|  | MOIntlCalls | int | 4 | NOT NULL |
|  | MOIntlDurSec | int | 4 | NOT NULL |
|  | MTCalls | int | 4 | NOT NULL |
|  | MTDurSec | int | 4 | NOT NULL |
|  | MTOnNetCalls | int | 4 | NOT NULL |
|  | MTOnNetDurSec | int | 4 | NOT NULL |
|  | MTOffNetCalls | int | 4 | NOT NULL |
|  | MTOffNetDurSec | int | 4 | NOT NULL |
|  | MTIntlCalls | int | 4 | NOT NULL |
|  | MTIntlDurSec | int | 4 | NOT NULL |
|  | SMO | int | 4 | NOT NULL |
|  | SMOOnNet | int | 4 | NOT NULL |
|  | SMOOffNet | int | 4 | NOT NULL |
|  | SMOIntl | int | 4 | NOT NULL |
|  | SMT | int | 4 | NOT NULL |
|  | SMTOnNet | int | 4 | NOT NULL |
|  | SMTOffNet | int | 4 | NOT NULL |
|  | SMTIntl | int | 4 | NOT NULL |
|  | USSD | int | 4 | NOT NULL |
|  | DataUpMb | numeric(18,6) | 9 | NULL allowed |
|  | DataDownMb | numeric(18,6) | 9 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerUsageDaily2 | IDDimDate, MSISDN | YES | MSC |
|  | IX_CustomerUsageDaily2 | MSISDN, IDDimDate |  | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[CustomerUsageDaily]](../Views/CustomerUsageDaily_000c.md)
* [[msc].[PyramidSubsDaily]](../Views/PyramidSubsDaily.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_000g.md)
* [[msc].[spc_LoadCustomerUsage_aux]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_aux.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

