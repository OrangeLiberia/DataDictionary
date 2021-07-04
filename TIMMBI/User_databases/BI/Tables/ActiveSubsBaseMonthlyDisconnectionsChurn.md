#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBaseMonthlyDisconnectionsChurn

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBaseMonthlyDisconnectionsChurn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthlyDisconnectionsChurn: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
| [![Primary Key PK_ActiveSubsBaseMonthlyDisconnectionsChurn: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL |
|  | Tenure | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBaseMonthlyDisconnectionsChurn: IDDimDate\MSISDN](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBaseMonthlyDisconnectionsChurn | IDDimDate, MSISDN | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

