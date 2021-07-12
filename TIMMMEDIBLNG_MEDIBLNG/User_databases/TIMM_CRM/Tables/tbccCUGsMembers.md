#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.tbccCUGsMembers

# ![Tables](../../../../Images/Table32.png) [dbo].[tbccCUGsMembers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tbccCUGsMembers: ID_CUG\ServiceID](../../../../Images/pkcluster.png)](#indexes) | ID_CUG | int | 4 | NOT NULL |
|  | Mainkey | varchar(20) | 20 | NOT NULL |
| [![Cluster Primary Key PK_tbccCUGsMembers: ID_CUG\ServiceID](../../../../Images/pkcluster.png)](#indexes) | ServiceID | numeric(18,0) | 9 | NOT NULL |
|  | DataInicio | datetime | 8 | NOT NULL |
|  | DataFim | datetime | 8 | NULL allowed |
|  | Estado | tinyint | 1 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

