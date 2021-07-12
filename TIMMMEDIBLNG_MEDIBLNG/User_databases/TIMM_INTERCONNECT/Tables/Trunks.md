#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Trunks

# ![Tables](../../../../Images/Table32.png) [dbo].[Trunks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Trunks_1: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_Trunks_Config_Central: [dbo].[Config_Central].ID_Central](../../../../Images/fk.png)](#foreignkeys) | ID_Central | int | 4 | NOT NULL |  |
|  | Trunk | varchar(50) | 50 | NOT NULL |  |
|  | Nome | varchar(50) | 50 | NULL allowed |  |
|  | Designacao | varchar(200) | 200 | NULL allowed |  |
| [![Foreign Keys FK_Trunks_TiposTrunk: [dbo].[TiposTrunk].Tipo](../../../../Images/fk.png)](#foreignkeys) | Tipo | tinyint | 1 | NOT NULL |  |
| [![Foreign Keys FK_Trunks_Rotas: [dbo].[Rotas].Rota_id](../../../../Images/fk.png)](#foreignkeys) | Rota_id | int | 4 | NOT NULL |  |
| [![Foreign Keys FK_Trunks_Operadoras: [dbo].[Operadoras].Operadora_id](../../../../Images/fk.png)](#foreignkeys) | Operadora_id | int | 4 | NOT NULL |  |
| [![Foreign Keys FK_Trunks_Config_Links: [dbo].[Config_Links].link_id](../../../../Images/fk.png)](#foreignkeys) | link_id | int | 4 | NOT NULL |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |
|  | StartTime | datetime | 8 | NULL allowed |  |
|  | EndTime | datetime | 8 | NULL allowed |  |
|  | Deleted | tinyint | 1 | NULL allowed |  |
|  | System | tinyint | 1 | NULL allowed |  |
|  | trunkID | bigint | 8 | NULL allowed |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Trunks_Config_Central | ID_Central->[[dbo].[Config_Central].[ID]](Config_Central.md) |
| FK_Trunks_Config_Links | link_id->[[dbo].[Config_Links].[ID]](Config_Links.md) |
| FK_Trunks_Operadoras | Operadora_id->[[dbo].[Operadoras].[ID]](Operadoras.md) |
| FK_Trunks_Rotas | Rota_id->[[dbo].[Rotas].[ID]](Rotas.md) |
| FK_Trunks_TiposTrunk | Tipo->[[dbo].[TiposTrunk].[ID]](TiposTrunk.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

