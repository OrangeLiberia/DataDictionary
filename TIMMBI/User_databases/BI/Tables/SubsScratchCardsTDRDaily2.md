#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsScratchCardsTDRDaily2

# ![Tables](../../../../Images/Table32.png) [in].[SubsScratchCardsTDRDaily2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |  |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | SubsId | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | SCAmount | numeric(24,6) | 13 | NOT NULL | _Scratch Card Amount (value)_ |
|  | Quantity | bigint | 8 | NOT NULL |  |
|  | TotalAmount | numeric(24,6) | 13 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | PK_SubsScratchCardsTDRDaily2 | IDDimDate, MSISDN, SubsId, SCAmount, WalletID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[SubsScratchCardsTDRDaily]](../Views/SubsScratchCardsTDRDaily.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spt_LoadSubsScratchCardsTDR]](../Programmability/Stored_Procedures/spt_LoadSubsScratchCardsTDR.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

