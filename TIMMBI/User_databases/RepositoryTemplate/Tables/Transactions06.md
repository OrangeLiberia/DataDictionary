#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > in.Transactions06

# ![Tables](../../../../Images/Table32.png) [in].[Transactions06]

---

## <a name="#description"></a>MS_Description

IN Transactions Day 06

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Indexes IX_Transactions06](../../../../Images/Index.png)](#indexes) | TransactionKey | int | 4 | NOT NULL | _Transaction Key_ |
|  | SubsId | int | 4 | NOT NULL | _IN Subscriber ID_ |
| [![Indexes IX_Transactions06](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(20) | 20 | NULL allowed | _Subscriber number_ |
|  | BMSISDN | varchar(20) | 20 | NULL allowed |  |
|  | ChargeableAmount | numeric(24,6) | 13 | NOT NULL | _Amount Charged_ |
| [![Indexes IX_Transactions06](../../../../Images/Index.png)](#indexes) | TDRTime | datetime | 8 | NOT NULL | _Date time of the transactions_ |
|  | CardSerialNumber | nvarchar(4000) | 8000 | NULL allowed | _Card serial number_ |
|  | TDREndingBalance | numeric(24,6) | 13 | NOT NULL | _Subscriber ending balance_ |
|  | WalletID | int | 4 | NOT NULL | _Wallet type ( ref. table [BI].[in].[WalletTypes] )_ |
|  | IN | tinyint | 1 | NOT NULL | _IN Identification (ref. table [BI].[in].[INs] )_ |
|  | ReferenceNumber | int | 4 | NULL allowed | _IN Reference number_ |
|  | CellID | int | 4 | NULL allowed | _Cell ID of the Call_ |
|  | IMEI | varchar(32) | 32 | NULL allowed | _IMEI_ |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns | File Group |
|---|---|---|
| IX_Transactions06 | TDRTime, MSISDN, TransactionKey | IN |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

