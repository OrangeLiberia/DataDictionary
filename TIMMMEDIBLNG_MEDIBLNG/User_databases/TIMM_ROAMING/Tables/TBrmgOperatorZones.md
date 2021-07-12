#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgOperatorZones

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgOperatorZones]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgOperatorZones_1: ZoneID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_TBrmgOperatorZones_Keys](../../../../Images/Index.png)](#indexes) | ZoneID | bigint | 8 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_TBrmgOperatorZones_Keys](../../../../Images/Index.png)](#indexes) | IDAgreement | bigint | 8 | NOT NULL |  | ((1)) |
|  | Keycode | varchar(50) | 50 | NULL allowed |  |  |
|  | LastuserID | int | 4 | NULL allowed |  |  |
|  | Lastupdate | datetime | 8 | NULL allowed |  | (getdate()) |
|  | Status | int | 4 | NULL allowed |  | ((1)) |
|  | DateBegin | datetime | 8 | NULL allowed |  |  |
|  | DateEnd | datetime | 8 | NULL allowed |  |  |
| [![Indexes IX_TBrmgOperatorZones_Keys](../../../../Images/Index.png)](#indexes)[![Foreign Keys FK_TBrmgOperatorZones_TbrmgTiposZonas: [dbo].[TbrmgTiposZonas].TiposZonasID](../../../../Images/fk.png)](#foreignkeys) | TiposZonasID | int | 4 | NULL allowed |  |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgOperatorZones_TbrmgTiposZonas | TiposZonasID->[[dbo].[TbrmgTiposZonas].[ID]](TbrmgTiposZonas.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

