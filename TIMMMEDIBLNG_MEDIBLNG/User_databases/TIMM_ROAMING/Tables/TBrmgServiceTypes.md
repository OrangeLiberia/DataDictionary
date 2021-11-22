#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgServiceTypes

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgServiceTypes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Indexes IX_TBrmgServiceTypes](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Cluster Primary Key PK_TBrmgServiceTypes: KeyService](../../../../Images/pkcluster.png)](#indexes) | KeyService | varchar(50) | 50 | NOT NULL |  |  |
|  | Descricao | varchar(500) | 500 | NOT NULL |  |  |
|  | KeyCodeLang | varchar(50) | 50 | NULL allowed |  |  |
|  | lastuserid | int | 4 | NOT NULL |  | ((0)) |
|  | lastupdate | datetime | 8 | NOT NULL |  | (getdate()) |
|  | status | bit | 1 | NOT NULL |  | ((1)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

