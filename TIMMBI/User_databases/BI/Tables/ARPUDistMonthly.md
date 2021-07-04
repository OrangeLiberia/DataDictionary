#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ARPUDistMonthly

# ![Tables](../../../../Images/Table32.png) [in].[ARPUDistMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDRange | int | 4 | NOT NULL |  |
|  | Range | varchar(30) | 30 | NOT NULL |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | Source | varchar(5) | 5 | NOT NULL |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDOrig | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | IDDest | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_ARPUDistMonthly: IDDimDate\IDRange\Type\Source\IDOrig\IDDest\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |  |
|  | NSubs | bigint | 8 | NOT NULL | ((0)) |
|  | NTotalCalls | bigint | 8 | NOT NULL | ((0)) |
|  | NChrgedCalls | bigint | 8 | NOT NULL | ((0)) |
|  | ChgbleAmount | float | 8 | NOT NULL | ((0)) |
|  | ChrgedCallsChgbleDuration | bigint | 8 | NOT NULL | ((0)) |
|  | ChrgedCallsRealDuration | bigint | 8 | NOT NULL | ((0)) |
|  | NFreeCalls | bigint | 8 | NOT NULL | ((0)) |
|  | FreeCallsChgbleDuration | bigint | 8 | NOT NULL | ((0)) |
|  | FreeCallsRealDuration | bigint | 8 | NOT NULL | ((0)) |
|  | RealDurationAmount | float | 8 | NOT NULL | ((0)) |


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

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

