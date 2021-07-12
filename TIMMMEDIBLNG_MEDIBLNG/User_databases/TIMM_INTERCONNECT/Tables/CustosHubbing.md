#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.CustosHubbing

# ![Tables](../../../../Images/Table32.png) [dbo].[CustosHubbing]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustosHubbing_1: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | nome | varchar(100) | 100 | NOT NULL |  |
|  | observacoes | varchar(2000) | 2000 | NULL allowed |  |
| [![Foreign Keys FK_custoshubbing_operadora: [dbo].[Operadoras].operadora_id](../../../../Images/fk.png)](#foreignkeys) | operadora_id | int | 4 | NOT NULL |  |
|  | FK_tipomoeda_id | int | 4 | NOT NULL |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |
|  | Archived | tinyint | 1 | NULL allowed |  |
|  | StartDate | datetime | 8 | NULL allowed |  |
|  | EndDate | datetime | 8 | NULL allowed |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_custoshubbing_operadora | operadora_id->[[dbo].[Operadoras].[ID]](Operadoras.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

