#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBaseMonthlyMarketShare

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBaseMonthlyMarketShare]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | TypeCDR | varchar(10) | 10 | NOT NULL |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | IDOrig | int | 4 | NOT NULL |
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | IDDest | int | 4 | NOT NULL |
|  | Calls | int | 4 | NULL allowed |
|  | SMS | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthlyMarketShare: IDDimDate\MSISDN\TypeCDR\IDOrig\IDDest](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBaseMonthlyMarketShare | IDDimDate, MSISDN, TypeCDR, IDOrig, IDDest | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

