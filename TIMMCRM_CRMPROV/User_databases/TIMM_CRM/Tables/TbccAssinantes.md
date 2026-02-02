#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccAssinantes

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccAssinantes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_TbccAssinantes_1: ServicoID](../../../../Images/pk.png)](#indexes) | ServicoID | numeric(18,0) | 9 | NOT NULL |
|  | NomeCompleto | varchar(200) | 200 | NULL allowed |
|  | NomeNaIN | varchar(20) | 20 | NULL allowed |
|  | TipoEntidade | tinyint | 1 | NULL allowed |
|  | NbrIdentidade | varchar(20) | 20 | NULL allowed |
|  | Morada | varchar(200) | 200 | NULL allowed |
|  | TipoRua | tinyint | 1 | NULL allowed |
|  | Lote | varchar(10) | 10 | NULL allowed |
|  | Andar | varchar(10) | 10 | NULL allowed |
|  | Localidade | varchar(200) | 200 | NULL allowed |
|  | CPostal | varchar(20) | 20 | NULL allowed |
|  | CPostalDesc | varchar(100) | 100 | NULL allowed |
|  | CodProvincia | tinyint | 1 | NULL allowed |
|  | CodPais | smallint | 2 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | AgenciaFilialID | numeric(18,0) | 9 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

