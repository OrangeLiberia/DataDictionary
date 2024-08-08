#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgSystemQuerys

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgSystemQuerys]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgQuerys: id](../../../../Images/pkcluster.png)](#indexes) | id | int | 4 | NOT NULL | 1 - 1 |  |
|  | type_id | int | 4 | NOT NULL |  |  |
|  | sp | varchar(200) | 200 | NOT NULL |  |  |
|  | description | varchar(50) | 50 | NULL allowed |  |  |
|  | xml_in | xml | max | NOT NULL |  |  |
|  | xml_out | xml | max | NULL allowed |  |  |
|  | usable | int | 4 | NOT NULL |  | ((0)) |
|  | legacy | bit | 1 | NULL allowed |  | ((0)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

