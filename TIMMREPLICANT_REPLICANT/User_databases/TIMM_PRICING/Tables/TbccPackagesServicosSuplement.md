#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccPackagesServicosSuplement

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccPackagesServicosSuplement]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccPackagesServicosSuplement: SSPackageID](../../../../Images/pkcluster.png)](#indexes) | SSPackageID | int | 4 | NOT NULL |
|  | SSPackageCod | varchar(12) | 12 | NOT NULL |
|  | SSPackageDesc | varchar(200) | 200 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | DataEfectiva | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

