#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Config_Tipo_QOS

# ![Tables](../../../../Images/Table32.png) [dbo].[Config_Tipo_QOS]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Config_Tipo_QOS: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Designacao | varchar(50) | 50 | NOT NULL |  |
|  | representacao | varchar(50) | 50 | NULL allowed |  |
| [![Foreign Keys FK_Config_Tipo_QOS_Config_TipoCalculo: [dbo].[Config_TipoCalculo].tipo_calculo](../../../../Images/fk.png)](#foreignkeys) | tipo_calculo | tinyint | 1 | NULL allowed |  |
|  | Keycode | varchar(max) | max | NULL allowed |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Config_Tipo_QOS_Config_TipoCalculo | tipo_calculo->[[dbo].[Config_TipoCalculo].[ID]](Config_TipoCalculo.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

