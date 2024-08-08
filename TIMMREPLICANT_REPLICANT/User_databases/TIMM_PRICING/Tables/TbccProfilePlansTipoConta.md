#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccProfilePlansTipoConta

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccProfilePlansTipoConta]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccProfilePlansTipoConta: ProfilePlanID\FK_TipoContaID](../../../../Images/pkcluster.png)](#indexes) | ProfilePlanID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccProfilePlansTipoConta: ProfilePlanID\FK_TipoContaID](../../../../Images/pkcluster.png)](#indexes) | FK_TipoContaID | int | 4 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | LastUserID | bigint | 8 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

