#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.QOS

# ![Tables](../../../../Images/Table32.png) [dbo].[QOS]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_qos: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_qos_operadora: [dbo].[Operadoras].operadora_id](../../../../Images/fk.png)](#foreignkeys) | operadora_id | int | 4 | NOT NULL |  |
| [![Foreign Keys FK_qos_rota: [dbo].[Rotas].rota_id](../../../../Images/fk.png)](#foreignkeys) | rota_id | int | 4 | NOT NULL |  |
|  | valor | float | 8 | NOT NULL |  |
|  | data_calculo | datetime | 8 | NOT NULL |  |
| [![Foreign Keys FK_QOS_Config_Tipo_QOS: [dbo].[Config_Tipo_QOS].tipo_qos_id](../../../../Images/fk.png)](#foreignkeys) | tipo_qos_id | int | 4 | NOT NULL |  |
|  | lastuserupdate | int | 4 | NULL allowed |  |
|  | lastdateupdate | datetime | 8 | NULL allowed |  |
| [![Foreign Keys FK_QOS_Trunks: [dbo].[Trunks].trunk_id](../../../../Images/fk.png)](#foreignkeys) | trunk_id | bigint | 8 | NOT NULL |  |
|  | Central_ID | int | 4 | NULL allowed |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_QOS_Config_Tipo_QOS | tipo_qos_id->[[dbo].[Config_Tipo_QOS].[ID]](Config_Tipo_QOS.md) |
| FK_qos_operadora | operadora_id->[[dbo].[Operadoras].[ID]](Operadoras.md) |
| FK_qos_rota | rota_id->[[dbo].[Rotas].[ID]](Rotas.md) |
| FK_QOS_Trunks | trunk_id->[[dbo].[Trunks].[ID]](Trunks.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

