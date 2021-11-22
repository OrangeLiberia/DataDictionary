#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CustomerUsageDaily2

# ![Tables](../../../../Images/Table32.png) [msc].[CustomerUsageDaily2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_CustomerUsageDaily2](../../../../Images/Index.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_CustomerUsageDaily2: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_CustomerUsageDaily2](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |  |
|  | IDOrigDest | int | 4 | NOT NULL |  |
|  | MOCalls | int | 4 | NOT NULL | _Number of MO calls_ |
|  | MODurSec | int | 4 | NOT NULL | _Duration of MO calls_ |
|  | MOOnNetCalls | int | 4 | NOT NULL | _Number of MO OnNet calls_ |
|  | MOOnNetDurSec | int | 4 | NOT NULL | _Duration of MO OnNet calls_ |
|  | MOOffNetCalls | int | 4 | NOT NULL | _Number of MO OffNet calls_ |
|  | MOOffNetDurSec | int | 4 | NOT NULL | _Duration of MO OffNet calls_ |
|  | MOIntlCalls | int | 4 | NOT NULL | _Number of MO International calls_ |
|  | MOIntlDurSec | int | 4 | NOT NULL | _Duration of MO International calls_ |
|  | MTCalls | int | 4 | NOT NULL | _Number of MT calls_ |
|  | MTDurSec | int | 4 | NOT NULL | _Duration of MT calls_ |
|  | MTOnNetCalls | int | 4 | NOT NULL | _Number of MT OnNet calls_ |
|  | MTOnNetDurSec | int | 4 | NOT NULL | _Duration of MT OnNet calls_ |
|  | MTOffNetCalls | int | 4 | NOT NULL | _Number of MT OffNet calls_ |
|  | MTOffNetDurSec | int | 4 | NOT NULL | _Duration of MT OffNet calls_ |
|  | MTIntlCalls | int | 4 | NOT NULL | _Number of MT International calls_ |
|  | MTIntlDurSec | int | 4 | NOT NULL | _Duration of MT International calls_ |
|  | SMO | int | 4 | NOT NULL | _Number of MO SMS_ |
|  | SMOOnNet | int | 4 | NOT NULL | _Number of MO OnNet SMS_ |
|  | SMOOffNet | int | 4 | NOT NULL | _Number of MO OffNet SMS_ |
|  | SMOIntl | int | 4 | NOT NULL | _Number of MO International SMS_ |
|  | SMT | int | 4 | NOT NULL | _Number of MT SMS_ |
|  | SMTOnNet | int | 4 | NOT NULL | _Number of MT OnNet SMS_ |
|  | SMTOffNet | int | 4 | NOT NULL | _Number of MT OffNet SMS_ |
|  | SMTIntl | int | 4 | NOT NULL | _Number of MT International SMS_ |
|  | USSD | int | 4 | NOT NULL |  |
|  | DataUpMb | numeric(18,6) | 9 | NULL allowed | _Total MB uploaded_ |
|  | DataDownMb | numeric(18,6) | 9 | NULL allowed | _Total MB downloaded_ |


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

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

