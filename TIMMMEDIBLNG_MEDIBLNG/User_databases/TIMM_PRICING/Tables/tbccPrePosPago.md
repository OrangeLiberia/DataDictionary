#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.tbccPrePosPago

# ![Tables](../../../../Images/Table32.png) [dbo].[tbccPrePosPago]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
|  | designacao | nvarchar(50) | 100 | NOT NULL |
|  | PrePago | bit | 1 | NULL allowed |
| [![Cluster Primary Key PK_tbccPrePosPago: ID](../../../../Images/pkcluster.png)](#indexes) | ID | tinyint | 1 | NOT NULL |
|  | KeyCode | varchar(256) | 256 | NOT NULL |
|  | DataRegisto | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NULL allowed |
|  | Status | tinyint | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

