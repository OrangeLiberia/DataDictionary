#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBaseMonthly

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBaseMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthly: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Primary Key PK_ActiveSubsBaseMonthly: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL |  |
|  | Active | tinyint | 1 | NULL allowed |  |
|  | MOCalls | int | 4 | NULL allowed | _Number of MO calls_ |
|  | MOSMS | int | 4 | NULL allowed |  |
|  | HasData | int | 4 | NULL allowed |  |
|  | VAS | int | 4 | NULL allowed |  |
|  | RoamingMO | int | 4 | NULL allowed |  |
|  | OM | int | 4 | NULL allowed |  |
|  | OutEvent | int | 4 | NULL allowed |  |
|  | MTCalls | int | 4 | NULL allowed | _Number of MT calls_ |
|  | MTSMS | int | 4 | NULL allowed |  |
|  | RoamingMT | int | 4 | NULL allowed |  |
|  | IncEvent | int | 4 | NULL allowed |  |
|  | Tenure | tinyint | 1 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthly: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBaseMonthly | IDDimDate, MSISDN | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

