#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubsScratchCardsTDRDaily2

# ![Tables](../../../../Images/Table32.png) [in].[SubsScratchCardsTDRDaily2]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | SubsId | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_SubsScratchCardsTDRDaily2: IDDimDate\MSISDN\SubsId\SCAmount\WalletID](../../../../Images/pkcluster.png)](#indexes) | SCAmount | numeric(24,6) | 13 | NOT NULL |
|  | Quantity | bigint | 8 | NOT NULL |
|  | TotalAmount | numeric(24,6) | 13 | NOT NULL |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

