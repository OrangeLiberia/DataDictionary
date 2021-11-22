#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.CallsOrigDestConfig

# ![Tables](../../../../Images/Table32.png) [in].[CallsOrigDestConfig]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsOrigDestConfig: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |  |
|  | Type | varchar(10) | 10 | NOT NULL |  |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
| [![Foreign Keys FK_CallsOrigDestConfig_CallsOrigDest: [fwk].[CallsOrigDest].IDOrigDest](../../../../Images/fk.png)](#foreignkeys) | IDOrigDest | int | 4 | NOT NULL |  |  |  |
|  | OrigMSISDNType | varchar(10) | 10 | NULL allowed |  |  |  |
|  | OrigMSISDN | varchar(20) | 20 | NULL allowed |  |  |  |
|  | OrigMSISDNSizeType | varchar(10) | 10 | NULL allowed |  |  |  |
|  | OrigMSISDNSize | tinyint | 1 | NULL allowed |  |  |  |
|  | TermMSISDNType | varchar(50) | 50 | NULL allowed |  |  |  |
|  | TermMSISDN | varchar(20) | 20 | NULL allowed |  |  |  |
|  | TermMSISDNSizeType | varchar(10) | 10 | NULL allowed |  |  |  |
|  | TermMSISDNSize | tinyint | 1 | NULL allowed |  |  |  |
|  | ServiceAccessCode | varchar(20) | 20 | NULL allowed |  |  |  |
|  | Order | smallint | 2 | NOT NULL |  | ((0)) |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  | (getdate()) |  |
|  | Status | smallint | 2 | NOT NULL |  | ((1)) |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsOrigDestConfig: ID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsOrigDestConfig | ID | YES | IN |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_CallsOrigDestConfig_CallsOrigDest | IDOrigDest->[[fwk].[CallsOrigDest].[ID]](CallsOrigDest.md) |


---

## <a name="#uses"></a>Uses

* [[fwk].[CallsOrigDest]](CallsOrigDest.md)
* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[spc_TransformationCallsDaily]](../Programmability/Stored_Procedures/spc_TransformationCallsDaily.md)
* [[in].[fnt_GetCallOrigDest]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetCallOrigDest.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

