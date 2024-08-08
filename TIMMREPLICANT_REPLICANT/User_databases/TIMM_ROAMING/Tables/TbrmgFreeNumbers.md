#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TbrmgFreeNumbers

# ![Tables](../../../../Images/Table32.png) [dbo].[TbrmgFreeNumbers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TbrmgFreeNumbers: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Number | varchar(32) | 32 | NOT NULL |  |
|  | Designacao | varchar(120) | 120 | NULL allowed |  |
|  | Active | tinyint | 1 | NOT NULL |  |
|  | ShowInTAP | tinyint | 1 | NOT NULL |  |
|  | ZoneID | varchar(50) | 50 | NULL allowed |  |
|  | LastUserID | int | 4 | NULL allowed |  |
|  | Lastupdate | datetime | 8 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

