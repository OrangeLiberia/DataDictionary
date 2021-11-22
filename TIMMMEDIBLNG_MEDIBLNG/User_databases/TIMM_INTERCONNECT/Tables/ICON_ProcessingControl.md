#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.ICON_ProcessingControl

# ![Tables](../../../../Images/Table32.png) [dbo].[ICON_ProcessingControl]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ICON_ProcessingControl: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Process | varchar(50) | 50 | NOT NULL |  |  |
|  | StartStep | int | 4 | NOT NULL |  |  |
|  | EndStep | int | 4 | NOT NULL |  |  |
|  | Enabled | bit | 1 | NOT NULL |  | ((1)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

