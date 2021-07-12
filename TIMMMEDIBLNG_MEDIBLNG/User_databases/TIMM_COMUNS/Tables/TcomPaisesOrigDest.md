#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomPaisesOrigDest

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomPaisesOrigDest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomPaisesOrigDest: CodPais](../../../../Images/pkcluster.png)](#indexes) | CodPais | varchar(10) | 10 | NOT NULL |
|  | Desig_Completa | varchar(50) | 50 | NOT NULL |
|  | Desig_Abrev | varchar(20) | 20 | NULL allowed |
|  | CCode | varchar(5) | 5 | NOT NULL |
|  | CodOrigDest | varchar(10) | 10 | NOT NULL |
|  | CodRoaming | varchar(50) | 50 | NULL allowed |
|  | IDUtilizador | int | 4 | NOT NULL |
|  | DataRegisto | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

