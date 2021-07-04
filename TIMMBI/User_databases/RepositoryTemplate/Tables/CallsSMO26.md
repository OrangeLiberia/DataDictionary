#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsSMO26

# ![Tables](../../../../Images/Table32.png) [msc].[CallsSMO26]

---

## <a name="#description"></a>MS_Description

MSC Mobile SMS Originator Calls Day 26

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsSMO26: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_CallsSMO26: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
|  | IMSI | varchar(32) | 32 | NULL allowed |
|  | IMEI | varchar(32) | 32 | NULL allowed |
|  | CALLINGNUMBER | varchar(32) | 32 | NULL allowed |
|  | CALLINGNUMBER_CC | varchar(6) | 6 | NULL allowed |
|  | CALLINGNUMBER_NDC | varchar(6) | 6 | NULL allowed |
|  | CALLEDNUMBER | varchar(32) | 32 | NULL allowed |
|  | CALLEDNUMBER_CC | varchar(6) | 6 | NULL allowed |
|  | CALLEDNUMBER_NDC | varchar(6) | 6 | NULL allowed |
|  | SMSTIMESTAMP | datetime | 8 | NULL allowed |
|  | DELIVERYTIMESTAMP | datetime | 8 | NULL allowed |
|  | CAUSEFORTERMINATION | smallint | 2 | NULL allowed |
|  | AMSISDN | varchar(32) | 32 | NULL allowed |
|  | BMSISDN | varchar(32) | 32 | NULL allowed |
|  | StartTime | datetime | 8 | NULL allowed |
|  | IDOrig | int | 4 | NULL allowed |
|  | IDDest | int | 4 | NULL allowed |
|  | IDTariff | int | 4 | NULL allowed |
|  | MSC | tinyint | 1 | NOT NULL |
|  | DuplicateCode | tinyint | 1 | NULL allowed |
|  | CellSectorID | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsSMO26: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsSMO26 | FileID, CDRID | YES | MSC |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

