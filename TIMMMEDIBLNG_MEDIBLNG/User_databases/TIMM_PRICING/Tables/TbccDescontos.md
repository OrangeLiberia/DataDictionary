#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccDescontos

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccDescontos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccDescontos: DescontoID](../../../../Images/pkcluster.png)](#indexes) | DescontoID | int | 4 | NOT NULL |
|  | DescontoCod | varchar(12) | 12 | NOT NULL |
|  | DescontoDesc | varchar(200) | 200 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | DataEfectiva | datetime | 8 | NOT NULL |
|  | PIincidenc | int | 4 | NOT NULL |
|  | TipoProfile | tinyint | 1 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | AgenciaFilialID | numeric(18,0) | 9 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

