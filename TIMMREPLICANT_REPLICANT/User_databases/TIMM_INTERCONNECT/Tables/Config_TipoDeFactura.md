#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Config_TipoDeFactura

# ![Tables](../../../../Images/Table32.png) [dbo].[Config_TipoDeFactura]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Config_TipoDeFactura: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Designacao | varchar(50) | 50 | NOT NULL |  |
| [![Foreign Keys FK_Config_TipoDeFactura_TcomTiposDocumento: [dbo].[TcomTiposDocumento].Tipo_Doc](../../../../Images/fk.png)](#foreignkeys) | Tipo_Doc | varchar(3) | 3 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Config_TipoDeFactura_TcomTiposDocumento | Tipo_Doc->[[dbo].[TcomTiposDocumento].[Tipo_Doc]](TcomTiposDocumento.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

