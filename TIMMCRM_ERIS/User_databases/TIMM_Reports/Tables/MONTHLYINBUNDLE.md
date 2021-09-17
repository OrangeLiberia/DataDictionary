#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.MONTHLYINBUNDLE

# ![Tables](../../../../Images/Table32.png) [dbo].[MONTHLYINBUNDLE]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__MONTHLYI__3214EC279ECB705D: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | MSISDN | varchar(32) | 32 | NOT NULL |  |
|  | TotalAmount | decimal(38,5) | 17 | NULL allowed |  |
|  | Bundle | varchar(200) | 200 | NULL allowed |  |
|  | Activations | int | 4 | NULL allowed |  |
|  | currency | varchar(8) | 8 | NULL allowed |  |
|  | REFMONTH | char(7) | 7 | NULL allowed |  |
|  | PARENT_NAME | varchar(200) | 200 | NULL allowed |  |
|  | PARENT_USER_MSISDN | varchar(15) | 15 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__MONTHLYI__3214EC279ECB705D: ID](../../../../Images/pkcluster.png)](#indexes) | PK__MONTHLYI__3214EC279ECB705D | ID | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

