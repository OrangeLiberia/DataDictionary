#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBaseMonthly30Days

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBaseMonthly30Days]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthly30Days: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Primary Key PK_ActiveSubsBaseMonthly30Days: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL |
|  | Active | tinyint | 1 | NULL allowed |
|  | MOCalls | int | 4 | NULL allowed |
|  | MOSMS | int | 4 | NULL allowed |
|  | HasData | int | 4 | NULL allowed |
|  | VAS | int | 4 | NULL allowed |
|  | RoamingMO | int | 4 | NULL allowed |
|  | OM | int | 4 | NULL allowed |
|  | OutEvent | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthly30Days: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBaseMonthly30Days | IDDimDate, MSISDN | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

