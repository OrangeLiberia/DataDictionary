#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsSMO01

# ![Tables](../../../../Images/Table32.png) [msc].[CallsSMO01]

---

## <a name="#description"></a>MS_Description

Originated SMS 

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsSMO01: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Mediation File ID_ |
| [![Cluster Primary Key PK_CallsSMO01: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL | _Mediation CDR ID_ |
|  | IMSI | varchar(32) | 32 | NULL allowed | _IMSI_ |
|  | IMEI | varchar(32) | 32 | NULL allowed | _IMEI_ |
|  | CALLINGNUMBER | varchar(32) | 32 | NULL allowed | _Calling Number_ |
|  | CALLINGNUMBER_CC | varchar(6) | 6 | NULL allowed | _Calling Number Country Code_ |
|  | CALLINGNUMBER_NDC | varchar(6) | 6 | NULL allowed | _Calling Number Network Destination Code_ |
|  | CALLEDNUMBER | varchar(32) | 32 | NULL allowed | _Called Number_ |
|  | CALLEDNUMBER_CC | varchar(6) | 6 | NULL allowed | _Called Number Country Code_ |
|  | CALLEDNUMBER_NDC | varchar(6) | 6 | NULL allowed | _Called Number Network Destination Code_ |
|  | SMSTIMESTAMP | datetime | 8 | NULL allowed | _SMS datetime_ |
|  | DELIVERYTIMESTAMP | datetime | 8 | NULL allowed | _SMS delivery datetime_ |
|  | CAUSEFORTERMINATION | smallint | 2 | NULL allowed | _SMS termination reason_ |
|  | AMSISDN | varchar(32) | 32 | NULL allowed | _Calling number_ |
|  | BMSISDN | varchar(32) | 32 | NULL allowed | _Called Number_ |
|  | StartTime | datetime | 8 | NULL allowed | _Start time_ |
|  | IDOrig | int | 4 | NULL allowed | _A MSISDN classification_ |
|  | IDDest | int | 4 | NULL allowed | _B MSISDN classification_ |
|  | IDTariff | int | 4 | NULL allowed |  |
|  | MSC | tinyint | 1 | NOT NULL |  |
|  | DuplicateCode | tinyint | 1 | NULL allowed |  |
|  | CellSectorID | int | 4 | NULL allowed | _Cell ID of the Call_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsSMO01: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsSMO01 | FileID, CDRID | YES | MSC |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

