#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccClientesEnderecos

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccClientesEnderecos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccClientesEnderecos_1: ClienteEnderecoID\ClienteID](../../../../Images/pkcluster.png)](#indexes) | ClienteEnderecoID | numeric(18,0) | 9 | NOT NULL |
| [![Cluster Primary Key PK_TbccClientesEnderecos_1: ClienteEnderecoID\ClienteID](../../../../Images/pkcluster.png)](#indexes) | ClienteID | numeric(18,0) | 9 | NOT NULL |
|  | Morada | varchar(200) | 200 | NOT NULL |
|  | TipoRua | tinyint | 1 | NOT NULL |
|  | Lote | varchar(10) | 10 | NULL allowed |
|  | Andar | varchar(10) | 10 | NULL allowed |
|  | Localidade | varchar(100) | 100 | NOT NULL |
|  | CPostal | varchar(20) | 20 | NULL allowed |
|  | CPostalDesc | varchar(20) | 20 | NULL allowed |
|  | CodProvincia | tinyint | 1 | NOT NULL |
|  | CodPais | int | 4 | NOT NULL |
|  | NbrFax | decimal(18,0) | 9 | NULL allowed |
|  | Email | varchar(200) | 200 | NULL allowed |
|  | NomeContacto | varchar(200) | 200 | NULL allowed |
|  | Nbr1Contacto | decimal(18,0) | 9 | NULL allowed |
|  | Nbr2Contacto | decimal(18,0) | 9 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | AgenciaFilialID | numeric(18,0) | 9 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | status | bit | 1 | NULL allowed |
|  | TipoMorada | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

