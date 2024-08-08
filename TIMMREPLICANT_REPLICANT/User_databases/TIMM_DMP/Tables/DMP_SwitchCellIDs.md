#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP](../index.md) > [Tables](Tables.md) > dbo.DMP_SwitchCellIDs

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_SwitchCellIDs]

---

## <a name="#description"></a>MS_Description

CellIDs Configuration Details per Switch

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Created | 9:33:41 AM Saturday, August 25, 2012 |
| Last Modified | 11:51:57 AM Tuesday, April 6, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_SwitchCellIDs: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Cell ID_ |
| [![Indexes idx_batchmode](../../../../Images/Index.png)](#indexes)[![Foreign Keys FK_DMP_SwitchCellIDs_DMP_SwitchConfig: [dbo].[DMP_SwitchConfig].SwitchID](../../../../Images/fk.png)](#foreignkeys) | SwitchID | int | 4 | NULL allowed | _SwitchID see [dbo.DMP_SwitchConfig](DMP_SwitchConfig.md)_ |
|  | SiteName | varchar(50) | 50 | NULL allowed | _Name of the Site_ |
|  | Location | int | 4 | NULL allowed | _Location of the Site_ |
|  | BSC | int | 4 | NULL allowed | _BSC ID_ |
|  | LACName | varchar(50) | 50 | NULL allowed | _Location Area Code_ |
|  | Latitude | numeric(8,6) | 5 | NULL allowed | _Latitude_ |
|  | Longitude | numeric(18,6) | 9 | NULL allowed | _Longitude_ |
|  | County | varchar(100) | 100 | NULL allowed | _County_ |
|  | City | varchar(128) | 128 | NULL allowed | _Ciry_ |
|  | Bourough | varchar(128) | 128 | NULL allowed | _Bourough_ |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_DMP_SwitchCellIDs_DMP_SwitchConfig | SwitchID->[[dbo].[DMP_SwitchConfig].[ID]](DMP_SwitchConfig.md) |


---

## <a name="#uses"></a>Uses

* [[dbo].[DMP_SwitchConfig]](DMP_SwitchConfig.md)


---

## <a name="#usedby"></a>Used By

* [TIMM_Reports].[dbo].[TDDB2CConsumption]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

