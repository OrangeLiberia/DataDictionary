#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.tcomClientesKYC

# ![Tables](../../../../Images/Table32.png) [dbo].[tcomClientesKYC]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tcomClientesKYC: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | Type | varchar(16) | 16 | NOT NULL |
|  | Name | varchar(200) | 200 | NOT NULL |
|  | KeyCode | varchar(200) | 200 | NULL allowed |
|  | ValidRegistration | int | 4 | NOT NULL |
|  | Valid | bit | 1 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

