#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBaseMonthlyMarketShare

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBaseMonthlyMarketShare]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL |  |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | TypeCDR | varchar(10) | 10 | NOT NULL |  |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | IDOrig | int | 4 | NOT NULL | _ID of the Calling Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | IDDest | int | 4 | NOT NULL | _ID of the Called Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
|  | Calls | int | 4 | NULL allowed |  |
|  | SMS | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBaseMonthlyMarketShare | IDDimDate, MSISDN, TypeCDR, IDOrig, IDDest | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

