#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP](../index.md) > [Tables](Tables.md) > dbo.DMP_SwitchConfig

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_SwitchConfig]

---

## <a name="#description"></a>MS_Description

Switch Configuration

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Created | 5:30:03 PM Monday, September 17, 2007 |
| Last Modified | 11:03:44 PM Tuesday, October 4, 2016 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_SwitchConfig: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |
|  | ID_Key | varchar(50) | 50 | NULL allowed |  |
|  | Manufacturer | varchar(50) | 50 | NULL allowed |  |
|  | Model | varchar(50) | 50 | NULL allowed |  |
|  | Shortname | varchar(50) | 50 | NOT NULL |  |
|  | LastuserID | int | 4 | NOT NULL |  |
|  | Lastupdate | smalldatetime | 4 | NOT NULL | (getdate()) |


---

## <a name="#usedby"></a>Used By

* [[dbo].[DMP_SwitchCellIDs]](DMP_SwitchCellIDs.md)
* [dbo].[TIMM_DMP_GetSwitchSources]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

