#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Config_TiposOTTrafego

# ![Tables](../../../../Images/Table32.png) [dbo].[Config_TiposOTTrafego]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Config_TiposOTTrafego: id](../../../../Images/pkcluster.png)](#indexes) | id | int | 4 | NOT NULL | 1 - 1 |
|  | bit_elemento | tinyint | 1 | NOT NULL |  |
|  | Ordem_avaliacao | tinyint | 1 | NULL allowed |  |
|  | elemento | varchar(50) | 50 | NOT NULL |  |
|  | KeyCode_ToolTip | nvarchar(max) | max | NULL allowed |  |
|  | KeyCode | varchar(50) | 50 | NULL allowed |  |
|  | SqlStatement | varchar(max) | max | NULL allowed |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |
|  | TrafficType | varchar(max) | max | NULL allowed |  |
|  | FixoMovel | tinyint | 1 | NULL allowed |  |
|  | VisivelFormTipos | tinyint | 1 | NULL allowed |  |
|  | VisivelFormAcordos | tinyint | 1 | NULL allowed |  |
|  | IDParent | int | 4 | NULL allowed |  |
|  | VisivelCMB | tinyint | 1 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

