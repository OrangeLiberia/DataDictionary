#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > in.CallsMO02

# ![Tables](../../../../Images/Table32.png) [in].[CallsMO02]

---

## <a name="#description"></a>MS_Description

IN Mobile Originated Calls Day 02

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
|  | SubsNumber | varchar(50) | 50 | NULL allowed | _Here is my description!_ |
|  | OriginDigits | varchar(50) | 50 | NULL allowed |  |
|  | DialedDigits | varchar(50) | 50 | NULL allowed |  |
| [![Indexes IX_CallsMO02](../../../../Images/Index.png)](#indexes) | AMSISDN | varchar(50) | 50 | NULL allowed |  |
| [![Indexes IX_CallsMO02](../../../../Images/Index.png)](#indexes) | BMSISDN | varchar(50) | 50 | NULL allowed |  |
|  | IDOrig | int | 4 | NULL allowed |  |
|  | IDDest | int | 4 | NULL allowed |  |
| [![Indexes IX_CallsMO02](../../../../Images/Index.png)](#indexes) | StartTime | datetime | 8 | NULL allowed |  |
|  | OriginateTime | datetime | 8 | NULL allowed |  |
|  | AnswerTime | datetime | 8 | NULL allowed |  |
|  | DisconnectTime | datetime | 8 | NULL allowed |  |
|  | ProductType | int | 4 | NOT NULL |  |
|  | DurSec | int | 4 | NULL allowed |  |
|  | ChargeableDuration | int | 4 | NULL allowed |  |
|  | AmountCharged | float | 8 | NULL allowed |  |
|  | RateDur | float | 8 | NULL allowed |  |
|  | EndingBalance | float | 8 | NULL allowed |  |
|  | WalletType | int | 4 | NULL allowed |  |
|  | ServiceAccessCode | varchar(20) | 20 | NULL allowed |  |
|  | IN | tinyint | 1 | NOT NULL |  |
|  | ReferenceNumber | int | 4 | NULL allowed |  |
|  | SubsID | int | 4 | NULL allowed |  |
|  | CellID | int | 4 | NULL allowed |  |
|  | IMEI | varchar(32) | 32 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns | File Group |
|---|---|---|
| IX_CallsMO02 | StartTime, AMSISDN, BMSISDN | IN |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

