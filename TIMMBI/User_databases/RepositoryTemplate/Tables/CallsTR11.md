#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsTR11

# ![Tables](../../../../Images/Table32.png) [msc].[CallsTR11]

---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsTR11: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_CallsTR11: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
|  | CALLINGNUMBER | varchar(32) | 32 | NULL allowed |
|  | CALLEDNUMBER | varchar(32) | 32 | NULL allowed |
|  | OUTTRUNKSEIZURE | datetime | 8 | NULL allowed |
|  | ANSWERTIME | datetime | 8 | NULL allowed |
|  | OUTTRUNKRELEASE | datetime | 8 | NULL allowed |
|  | CAUSEFORTERMINATION | smallint | 2 | NULL allowed |
|  | INTRUNKGROUP | int | 4 | NULL allowed |
|  | OUTTRUNKGROUP | int | 4 | NULL allowed |
|  | CallDuration | int | 4 | NULL allowed |
|  | DurSecBill | int | 4 | NULL allowed |
|  | RateDur | float | 8 | NULL allowed |
|  | RateBill | float | 8 | NULL allowed |
|  | RateIconRoam | float | 8 | NULL allowed |
|  | AMSISDN | varchar(32) | 32 | NULL allowed |
|  | BMSISDN | varchar(32) | 32 | NULL allowed |
|  | StartTime | datetime | 8 | NULL allowed |
|  | IDOrig | int | 4 | NULL allowed |
|  | IDDest | int | 4 | NULL allowed |
|  | IDTariff | int | 4 | NULL allowed |
|  | IDTariffIconRoam | int | 4 | NULL allowed |
|  | MSC | tinyint | 1 | NOT NULL |
|  | DuplicateCode | tinyint | 1 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CallsTR11: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes) | PK_CallsTR11 | FileID, CDRID | YES | MSC |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

