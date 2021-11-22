#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Acordos

# ![Tables](../../../../Images/Table32.png) [dbo].[Acordos]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Acordos_1: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | data_do_inicio | datetime | 8 | NOT NULL |  |
|  | data_fim | datetime | 8 | NOT NULL |  |
| [![Foreign Keys FK_Acordos_TipodeAcordo: [dbo].[Acordos_Tipo].acordos_tipo_id](../../../../Images/fk.png)](#foreignkeys) | acordos_tipo_id | int | 4 | NOT NULL |  |
| [![Foreign Keys FK_Acordos_Operadoras: [dbo].[Operadoras].operadora_id](../../../../Images/fk.png)](#foreignkeys) | operadora_id | int | 4 | NOT NULL |  |
|  | extensivel | bit | 1 | NOT NULL |  |
|  | inactivo | bit | 1 | NOT NULL |  |
|  | eliminado | bit | 1 | NOT NULL |  |
|  | acordo_xml | xml | max | NOT NULL |  |
|  | tipoimposto_id | int | 4 | NOT NULL |  |
| [![Foreign Keys FK_Acordos_Config_TipoDeFactura: [dbo].[Config_TipoDeFactura].tipofacturacao_id](../../../../Images/fk.png)](#foreignkeys) | tipofacturacao_id | int | 4 | NOT NULL |  |
|  | moedatipo_id | int | 4 | NOT NULL |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Acordos_Config_TipoDeFactura | tipofacturacao_id->[[dbo].[Config_TipoDeFactura].[ID]](Config_TipoDeFactura.md) |
| FK_Acordos_Operadoras | operadora_id->[[dbo].[Operadoras].[ID]](Operadoras.md) |
| FK_Acordos_TipodeAcordo | acordos_tipo_id->[[dbo].[Acordos_Tipo].[id]](Acordos_Tipo.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

