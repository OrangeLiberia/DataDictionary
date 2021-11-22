#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsMO06

# ![Tables](../../../../Images/Table32.png) [msc].[CallsMO06]

---

## <a name="#description"></a>MS_Description

MSC Mobile Originator Calls Day 06

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsMO06: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Mediation File ID_ |
| [![Cluster Primary Key PK_CallsMO06: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL | _Mediation CDR ID_ |
|  | IMSI | varchar(32) | 32 | NULL allowed | _IMSI_ |
|  | IMEI | varchar(32) | 32 | NULL allowed | _IMEI_ |
|  | CALLINGNUMBER | varchar(32) | 32 | NULL allowed | _Calling Number_ |
|  | CALLINGNUMBER_CC | varchar(6) | 6 | NULL allowed | _Calling Number Country Code_ |
|  | CALLINGNUMBER_NDC | varchar(6) | 6 | NULL allowed | _Calling Number Network Destination Code_ |
|  | CALLEDNUMBER | varchar(32) | 32 | NULL allowed | _Called Number_ |
|  | DIALEDDIGITS | varchar(32) | 32 | NULL allowed | _Dialed Digits_ |
|  | CALLEDNUMBER_CC | varchar(6) | 6 | NULL allowed | _Called Number Country Code_ |
|  | CALLEDNUMBER_NDC | varchar(6) | 6 | NULL allowed | _Called Number Network Destination Code_ |
|  | CHALLOCTIME | datetime | 8 | NULL allowed | _Seizure datetime_ |
|  | ANSWERTIME | datetime | 8 | NULL allowed | _Answer datetime_ |
|  | DISCONNECTTIME | datetime | 8 | NULL allowed | _Disconnect datetime_ |
|  | RELEASETIME | datetime | 8 | NULL allowed | _Release datetime_ |
|  | CLASSMARKTIME | datetime | 8 | NULL allowed |  |
|  | OUTTRUNKSEIZURE | datetime | 8 | NULL allowed | _Out Trunk Seizure datetime_ |
|  | OUTTRUNKGROUP | int | 4 | NULL allowed | _Out Trunk Group_ |
|  | CallDuration | int | 4 | NULL allowed | _Call Duration (seconds)_ |
|  | CAUSEFORTERMINATION | smallint | 2 | NULL allowed | _Call termination reason_ |
|  | DIAG_ERRCOD | smallint | 2 | NULL allowed | _Call Diagnostics _ |
|  | MSCLASSMARK | varchar(32) | 32 | NULL allowed |  |
|  | CALLINGSUBSCRIBERCAT | smallint | 2 | NULL allowed |  |
|  | DurSecBill | int | 4 | NULL allowed |  |
|  | RateDur | float | 8 | NULL allowed |  |
|  | RateBill | float | 8 | NULL allowed |  |
|  | RateIconRoam | float | 8 | NULL allowed |  |
|  | AMSISDN | varchar(32) | 32 | NULL allowed | _Calling number_ |
|  | BMSISDN | varchar(32) | 32 | NULL allowed | _Called Number_ |
|  | StartTime | datetime | 8 | NULL allowed | _Start time_ |
|  | COSID | int | 4 | NULL allowed | _Class of Service ID_ |
|  | IDOrig | int | 4 | NULL allowed | _A MSISDN classification_ |
|  | IDDest | int | 4 | NULL allowed | _B MSISDN classification_ |
|  | IDTariff | int | 4 | NULL allowed |  |
|  | IDTariffIconRoam | int | 4 | NULL allowed |  |
|  | DuplicateCode | tinyint | 1 | NULL allowed |  |
|  | MSC | tinyint | 1 | NOT NULL |  |
|  | CalledIMEI | varchar(32) | 32 | NULL allowed | _Called IMEI_ |
|  | CalledIMSI | varchar(32) | 32 | NULL allowed | _Called IMSI_ |
|  | CellSectorID | int | 4 | NULL allowed | _Cell ID of the Call_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsMO06: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsMO06 | FileID, CDRID | YES | MSC |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

