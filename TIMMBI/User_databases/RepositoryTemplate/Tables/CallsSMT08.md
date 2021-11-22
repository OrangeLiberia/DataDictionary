#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsSMT08

# ![Tables](../../../../Images/Table32.png) [msc].[CallsSMT08]

---

## <a name="#description"></a>MS_Description

MSC Mobile SMS Terminator Day 08

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsSMT08: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_CallsSMT08: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
|  | IMSI | varchar(32) | 32 | NULL allowed |
|  | IMEI | varchar(32) | 32 | NULL allowed |
|  | CALLINGNUMBER | varchar(32) | 32 | NULL allowed |
|  | CALLINGNUMBER_CC | varchar(6) | 6 | NULL allowed |
|  | CALLINGNUMBER_NDC | varchar(6) | 6 | NULL allowed |
|  | CALLEDNUMBER | varchar(32) | 32 | NULL allowed |
|  | CALLEDNUMBER_CC | varchar(6) | 6 | NULL allowed |
|  | CALLEDNUMBER_NDC | varchar(6) | 6 | NULL allowed |
|  | DISCONNECTTIME | datetime | 8 | NULL allowed |
|  | RELEASETIME | datetime | 8 | NULL allowed |
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
| [![Cluster Primary Key PK_CallsSMT08: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsSMT08 | FileID, CDRID | YES | MSC |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

