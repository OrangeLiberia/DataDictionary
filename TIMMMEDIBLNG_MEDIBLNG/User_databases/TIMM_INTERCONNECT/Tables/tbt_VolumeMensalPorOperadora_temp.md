#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_VolumeMensalPorOperadora_temp

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_VolumeMensalPorOperadora_temp]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_VolumeMensalPorOperadora_temp: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Mes | int | 4 | NOT NULL |  |  |
|  | Ano | int | 4 | NOT NULL |  |  |
|  | Operadora_ID | int | 4 | NOT NULL |  |  |
|  | VolumeMinutosEntrada | float | 8 | NOT NULL |  |  |
|  | CallIn | int | 4 | NULL allowed |  |  |
|  | VolumeMinutosSaida | float | 8 | NOT NULL |  |  |
|  | CallOut | int | 4 | NULL allowed |  |  |
|  | Documento_ID | int | 4 | NULL allowed |  |  |
|  | Documento_State | varchar(max) | max | NULL allowed |  |  |
|  | RepStatus | varchar(max) | max | NULL allowed |  |  |
|  | ExpStatus | varchar(max) | max | NULL allowed |  |  |
|  | lastuserupdate | int | 4 | NULL allowed |  |  |
|  | lastdateupdate | datetime | 8 | NULL allowed |  | (getdate()) |
|  | createddate | datetime | 8 | NULL allowed |  | (getdate()) |
|  | Tipo_Servico_ID | int | 4 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

