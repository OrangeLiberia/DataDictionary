#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccClientes

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccClientes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccClientes: ClienteID](../../../../Images/pkcluster.png)](#indexes) | ClienteID | numeric(18,0) | 9 | NOT NULL |
|  | NomeCompleto | varchar(200) | 200 | NOT NULL |
|  | ClienteIDUPPER | numeric(18,0) | 9 | NULL allowed |
|  | TipoIdentidade | tinyint | 1 | NULL allowed |
|  | NBRIdentidade | varchar(20) | 20 | NULL allowed |
|  | TipoCliente | tinyint | 1 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | AgenciaFilialID | numeric(18,0) | 9 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | IDSexo | smallint | 2 | NULL allowed |
|  | IDRate | int | 4 | NULL allowed |
|  | Status | bit | 1 | NULL allowed |
|  | DataNascimento | datetime | 8 | NULL allowed |
|  | LocalDeNascimento | varchar(100) | 100 | NULL allowed |
|  | ProfissaoID | int | 4 | NULL allowed |
|  | CountryOfOriginID | int | 4 | NULL allowed |
|  | Nacionality | varchar(150) | 150 | NULL allowed |
|  | Registration | tinyint | 1 | NULL allowed |
|  | Data1 | varchar(max) | max | NULL allowed |
|  | Data2 | varchar(max) | max | NULL allowed |
|  | Data3 | varchar(max) | max | NULL allowed |
|  | Data4 | varchar(max) | max | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

