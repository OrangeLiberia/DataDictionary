#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CallsDistMonthly

# ![Tables](../../../../Images/Table32.png) [msc].[CallsDistMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistMonthly: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistMonthly: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_CallsDistMonthly: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistMonthly: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | IDDest | int | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CallsDistMonthly: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | MSC | tinyint | 1 | NOT NULL |  | _MSC ID (see [msc.INs](MSCs.md))_ |
|  | NCalls0Dur | bigint | 8 | NOT NULL | ((0)) | _Number of calls with 0 duration_ |
|  | NCallsDur | bigint | 8 | NOT NULL | ((0)) | _Number of calls with duration_ |
|  | DurSec | bigint | 8 | NOT NULL | ((0)) | _Duration in seconds_ |
|  | DurSecBill | bigint | 8 | NOT NULL | ((0)) | _Duration in seconds_ |
|  | RateDur | float | 8 | NOT NULL | ((0)) |  |
|  | RateBill | float | 8 | NOT NULL | ((0)) |  |
|  | RateIconRoam | float | 8 | NOT NULL | ((0)) |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistMonthly: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | PK_CallsDistMonthly | IDDimDate, Type, IDOrig, IDDest, MSC | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spt_GetINMSCMonthlyComparison]](../Programmability/Stored_Procedures/spt_GetINMSCMonthlyComparison.md)
* [[msc].[spt_LoadCallsDist]](../Programmability/Stored_Procedures/spt_LoadCallsDist_000j.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

