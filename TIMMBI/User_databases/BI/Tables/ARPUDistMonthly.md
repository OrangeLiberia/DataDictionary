#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ARPUDistMonthly

# ![Tables](../../../../Images/Table32.png) [in].[ARPUDistMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDRange | int | 4 | NOT NULL |  | _ID of the ARPU Range (see [in.ARPURanges](ARPURanges.md))_ |
|  | Range | varchar(30) | 30 | NOT NULL |  |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | Source | varchar(5) | 5 | NOT NULL |  | _Source of the data_ |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int | 4 | NOT NULL |  | _ID of the Calling Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDest | int | 4 | NOT NULL |  | _ID of the Called Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |  | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
|  | NSubs | bigint | 8 | NOT NULL | ((0)) | _Number of subscribers_ |
|  | NTotalCalls | bigint | 8 | NOT NULL | ((0)) | _Number of total calls_ |
|  | NChrgedCalls | bigint | 8 | NOT NULL | ((0)) | _Number of charged calls_ |
|  | ChgbleAmount | float | 8 | NOT NULL | ((0)) | _Amount charged_ |
|  | ChrgedCallsChgbleDuration | bigint | 8 | NOT NULL | ((0)) | _Rounded Duration of charged calls_ |
|  | ChrgedCallsRealDuration | bigint | 8 | NOT NULL | ((0)) | _Real Duration of charged calls_ |
|  | NFreeCalls | bigint | 8 | NOT NULL | ((0)) | _Number of free calls_ |
|  | FreeCallsChgbleDuration | bigint | 8 | NOT NULL | ((0)) | _Rounded Duration of free calls_ |
|  | FreeCallsRealDuration | bigint | 8 | NOT NULL | ((0)) | _Real Duration of free calls_ |
|  | RealDurationAmount | float | 8 | NOT NULL | ((0)) | _Amount calculated of real duration_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | PK_ARPUDistMonthly | IDDimDate, IDRange, Type, Source, IDOrig, IDDest, WalletID | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[in].[spc_GetARPUDistMonthly]](../Programmability/Stored_Procedures/spc_GetARPUDistMonthly.md)
* [[in].[spc_GetARPUDistMonthlyDetails]](../Programmability/Stored_Procedures/spc_GetARPUDistMonthlyDetails.md)
* [[in].[spt_LoadARPUDistMonthly]](../Programmability/Stored_Procedures/spt_LoadARPUDistMonthly.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

