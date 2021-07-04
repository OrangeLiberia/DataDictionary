#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._143_ActivityOrange

# ![Tables](../../../../Images/Table32.png) [dbo].[_143_ActivityOrange]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_143_ActivityOrange: MSISDN\IDDimDate](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |
| [![Cluster Primary Key PK_143_ActivityOrange: MSISDN\IDDimDate](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | Month | date | 3 | NOT NULL |
|  | N143SMSs | bigint | 8 | NULL allowed |
|  | N143Calls | bigint | 8 | NULL allowed |
|  | 143RealSeconds | float | 8 | NULL allowed |
|  | 143BillSeconds | float | 8 | NULL allowed |
|  | 143FeeAmount | float | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_143_ActivityOrange: MSISDN\IDDimDate](../../../../Images/pkcluster.png)](#indexes) | PK_143_ActivityOrange | MSISDN, IDDimDate | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

