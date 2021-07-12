#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Classificacao_trafego

# ![Tables](../../../../Images/Table32.png) [dbo].[Classificacao_trafego]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_classificacao_trafego: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_classificacao_trafego_Config_TiposOTTrafego: [dbo].[Config_TiposOTTrafego].elemento_id](../../../../Images/fk.png)](#foreignkeys) | elemento_id | int | 4 | NOT NULL |  |
|  | acordo_id | bigint | 8 | NOT NULL |  |
|  | FK_View_Match | varchar(50) | 50 | NOT NULL |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_classificacao_trafego_Config_TiposOTTrafego | elemento_id->[[dbo].[Config_TiposOTTrafego].[id]](Config_TiposOTTrafego.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

