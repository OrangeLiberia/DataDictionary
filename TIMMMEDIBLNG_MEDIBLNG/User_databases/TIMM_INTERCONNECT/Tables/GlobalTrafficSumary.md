#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.GlobalTrafficSumary

# ![Tables](../../../../Images/Table32.png) [dbo].[GlobalTrafficSumary]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_GlobalTrafficSumary: Period\ServiceType\Route\InOperator\OutOperator](../../../../Images/pkcluster.png)](#indexes) | Period | varchar(6) | 6 | NOT NULL |
| [![Cluster Primary Key PK_GlobalTrafficSumary: Period\ServiceType\Route\InOperator\OutOperator](../../../../Images/pkcluster.png)](#indexes) | ServiceType | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_GlobalTrafficSumary: Period\ServiceType\Route\InOperator\OutOperator](../../../../Images/pkcluster.png)](#indexes) | Route | varchar(128) | 128 | NOT NULL |
| [![Cluster Primary Key PK_GlobalTrafficSumary: Period\ServiceType\Route\InOperator\OutOperator](../../../../Images/pkcluster.png)](#indexes) | InOperator | varchar(128) | 128 | NOT NULL |
| [![Cluster Primary Key PK_GlobalTrafficSumary: Period\ServiceType\Route\InOperator\OutOperator](../../../../Images/pkcluster.png)](#indexes) | OutOperator | varchar(128) | 128 | NOT NULL |
|  | Minutes | numeric(25,8) | 13 | NOT NULL |
|  | Calls | bigint | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

