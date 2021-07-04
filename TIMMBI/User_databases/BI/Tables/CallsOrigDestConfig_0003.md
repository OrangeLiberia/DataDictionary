#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CallsOrigDestConfig

# ![Tables](../../../../Images/Table32.png) [msc].[CallsOrigDestConfig]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsOrigDestConfig: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Type | varchar(10) | 10 | NOT NULL |  |  |
| [![Foreign Keys FK_CallsOrigDestConfig_CallsOrigDest: [fwk].[CallsOrigDest].IDOrigDest](../../../../Images/fk.png)](#foreignkeys) | IDOrigDest | int | 4 | NOT NULL |  |  |
|  | TrunkOutType | varchar(5) | 5 | NULL allowed |  |  |
|  | TrunkOut | varchar(10) | 10 | NULL allowed |  |  |
|  | TrunkOutSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | TrunkOutSize | tinyint | 1 | NULL allowed |  |  |
|  | TrunkInType | varchar(50) | 50 | NULL allowed |  |  |
|  | TrunkIn | varchar(10) | 10 | NULL allowed |  |  |
|  | TrunkInSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | TrunkInSize | tinyint | 1 | NULL allowed |  |  |
|  | OrigCCType | varchar(50) | 50 | NULL allowed |  |  |
|  | OrigCC | varchar(6) | 6 | NULL allowed |  |  |
|  | OrigCCSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | OrigCCSize | tinyint | 1 | NULL allowed |  |  |
|  | OrigNDCType | varchar(50) | 50 | NULL allowed |  |  |
|  | OrigNDC | varchar(6) | 6 | NULL allowed |  |  |
|  | OrigNDCSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | OrigNDCSize | tinyint | 1 | NULL allowed |  |  |
|  | OrigMSISDNType | varchar(50) | 50 | NULL allowed |  |  |
|  | OrigMSISDN | varchar(20) | 20 | NULL allowed |  |  |
|  | OrigMSISDNSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | OrigMSISDNSize | tinyint | 1 | NULL allowed |  |  |
|  | TermCCType | varchar(50) | 50 | NULL allowed |  |  |
|  | TermCC | varchar(6) | 6 | NULL allowed |  |  |
|  | TermCCSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | TermCCSize | tinyint | 1 | NULL allowed |  |  |
|  | TermNDCType | varchar(50) | 50 | NULL allowed |  |  |
|  | TermNDC | varchar(6) | 6 | NULL allowed |  |  |
|  | TermNDCSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | TermNDCSize | tinyint | 1 | NULL allowed |  |  |
|  | TermMSISDNType | varchar(50) | 50 | NULL allowed |  |  |
|  | TermMSISDN | varchar(20) | 20 | NULL allowed |  |  |
|  | TermMSISDNSizeType | varchar(10) | 10 | NULL allowed |  |  |
|  | TermMSISDNSize | tinyint | 1 | NULL allowed |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  | (getdate()) |
|  | Status | smallint | 2 | NOT NULL |  | ((1)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsOrigDestConfig: ID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsOrigDestConfig | ID | YES | MSC |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_CallsOrigDestConfig_CallsOrigDest | IDOrigDest->[[fwk].[CallsOrigDest].[ID]](CallsOrigDest.md) |


---

## <a name="#uses"></a>Uses

* [[fwk].[CallsOrigDest]](CallsOrigDest.md)
* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[spc_GetCallsDistribution]](../Programmability/Stored_Procedures/spc_GetCallsDistribution.md)
* [[msc].[spc_TransformationCallsDaily]](../Programmability/Stored_Procedures/spc_TransformationCallsDaily_000i.md)
* [[msc].[fnt_GetCallOrigDest]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetCallOrigDest_000m.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

