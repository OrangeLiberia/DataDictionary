#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CallsDistDaily

# ![Tables](../../../../Images/Table32.png) [msc].[CallsDistDaily]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | IDDest | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | MSC | tinyint | 1 | NOT NULL |  |
|  | NCalls0Dur | bigint | 8 | NOT NULL | ((0)) |
|  | NCallsDur | bigint | 8 | NOT NULL | ((0)) |
|  | DurSec | bigint | 8 | NOT NULL | ((0)) |
|  | DurSecBill | bigint | 8 | NOT NULL | ((0)) |
|  | RateDur | float | 8 | NOT NULL | ((0)) |
|  | RateBill | float | 8 | NOT NULL | ((0)) |
|  | RateIconRoam | float | 8 | NOT NULL | ((0)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsDistDaily: IDDimDate\Type\IDOrig\IDDest\MSC](../../../../Images/pkcluster.png)](#indexes) | PK_CallsDistDaily | IDDimDate, Type, IDOrig, IDDest, MSC | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_GetCallsDistribution]](../Programmability/Stored_Procedures/spc_GetCallsDistribution.md)
* [[msc].[spt_GetINMSCDailyComparison]](../Programmability/Stored_Procedures/spt_GetINMSCDailyComparison.md)
* [[msc].[spt_LoadCallsDist]](../Programmability/Stored_Procedures/spt_LoadCallsDist_000j.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

