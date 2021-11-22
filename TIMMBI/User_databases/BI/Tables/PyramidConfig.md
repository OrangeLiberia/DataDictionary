#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.PyramidConfig

# ![Tables](../../../../Images/Table32.png) [msc].[PyramidConfig]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default | Description |
|---|---|---|---|---|---|---|---|
|  | ID | int | 4 | NOT NULL | 1 - 1 |  |  |
| [![Cluster Primary Key PK_PyramidConfig: Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
| [![Cluster Primary Key PK_PyramidConfig: Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | IDOrigDest | int | 4 | NOT NULL |  |  |  |
|  | Include0Dur | bit | 1 | NULL allowed |  | ((1)) |  |
|  | Status | bit | 1 | NULL allowed |  | ((0)) |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_PyramidConfig: Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | PK_PyramidConfig | Type, IDOrigDest | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[spc_LoadCustomerUsage]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_000g.md)
* [[msc].[spc_LoadCustomerUsage_aux]](../Programmability/Stored_Procedures/spc_LoadCustomerUsage_aux.md)
* [[msc].[spt_LoadPyramidSubs]](../Programmability/Stored_Procedures/spt_LoadPyramidSubs.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

