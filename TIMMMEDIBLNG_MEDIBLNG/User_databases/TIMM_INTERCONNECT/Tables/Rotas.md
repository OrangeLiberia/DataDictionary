#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Rotas

# ![Tables](../../../../Images/Table32.png) [dbo].[Rotas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_rota: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | designacao | nvarchar(50) | 100 | NOT NULL |  |  |
| [![Foreign Keys FK_Rotas_Operadoras: [dbo].[Operadoras].operadora_id](../../../../Images/fk.png)](#foreignkeys) | operadora_id | int | 4 | NULL allowed |  |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |  |
|  | deleted | bit | 1 | NOT NULL |  | ((0)) |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Rotas_Operadoras | operadora_id->[[dbo].[Operadoras].[ID]](Operadoras.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

