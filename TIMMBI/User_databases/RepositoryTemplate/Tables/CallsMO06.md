#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > in.CallsMO06

# ![Tables](../../../../Images/Table32.png) [in].[CallsMO06]

---

## <a name="#description"></a>MS_Description

IN Mobile Originated Calls Day 06

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
|  | SubsNumber | varchar(50) | 50 | NULL allowed | _Subscriber number_ |
|  | OriginDigits | varchar(50) | 50 | NULL allowed |  |
|  | DialedDigits | varchar(50) | 50 | NULL allowed | _Dialed Digits_ |
| [![Indexes IX_CallsMO06](../../../../Images/Index.png)](#indexes) | AMSISDN | varchar(50) | 50 | NULL allowed | _Calling number_ |
| [![Indexes IX_CallsMO06](../../../../Images/Index.png)](#indexes) | BMSISDN | varchar(50) | 50 | NULL allowed | _Called Number_ |
|  | IDOrig | int | 4 | NULL allowed | _A MSISDN classification_ |
|  | IDDest | int | 4 | NULL allowed | _B MSISDN classification_ |
| [![Indexes IX_CallsMO06](../../../../Images/Index.png)](#indexes) | StartTime | datetime | 8 | NULL allowed | _Call start time_ |
|  | OriginateTime | datetime | 8 | NULL allowed | _Originated start time_ |
|  | AnswerTime | datetime | 8 | NULL allowed | _Answer time_ |
|  | DisconnectTime | datetime | 8 | NULL allowed | _Disconnected time_ |
|  | ProductType | int | 4 | NOT NULL | _Product type_ |
|  | DurSec | int | 4 | NULL allowed | _Call duration_ |
|  | ChargeableDuration | int | 4 | NULL allowed | _Chargeable Call duration_ |
|  | AmountCharged | float | 8 | NULL allowed | _Amount Charged_ |
|  | RateDur | float | 8 | NULL allowed |  |
|  | EndingBalance | float | 8 | NULL allowed | _Subscriber ending balance_ |
|  | WalletType | int | 4 | NULL allowed | _Wallet type ( ref. table [BI].[in].[WalletTypes] )_ |
|  | ServiceAccessCode | varchar(20) | 20 | NULL allowed |  |
|  | IN | tinyint | 1 | NOT NULL | _IN Identification (ref. table [BI].[in].[INs] )_ |
|  | ReferenceNumber | int | 4 | NULL allowed | _IN Reference number_ |
|  | SubsID | int | 4 | NULL allowed | _IN Subscriber ID_ |
|  | CellID | int | 4 | NULL allowed | _Cell ID of the Call_ |
|  | IMEI | varchar(32) | 32 | NULL allowed | _IMEI_ |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns | File Group |
|---|---|---|
| IX_CallsMO06 | StartTime, AMSISDN, BMSISDN | IN |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

