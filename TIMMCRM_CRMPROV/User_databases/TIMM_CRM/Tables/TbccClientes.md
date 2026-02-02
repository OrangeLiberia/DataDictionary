#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccClientes

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccClientes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Description | References |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccClientes: ClienteID](../../../../Images/pkcluster.png)](#indexes) | ClienteID | numeric(18,0) | **Primary Key**. Unique identifier for the customer. |
|  | NomeCompleto | varchar(200) |Customer's full legal name. |
|  | ClienteIDUPPER | numeric(18,0) | Parent/Master Client ID for corporate hierarchies. |
|  | TipoIdentidade | tinyint | ID Document Type (e.g., Passport, National ID, Driver's License). | References [TIMM_COMUNS].[dbo].[TcomTiposIdentificacao]
|  | NBRIdentidade | varchar(20) | ID Document Number. |
|  | TipoCliente | tinyint | Customer segment/type (e.g., Individual, Corporate, Staff). | References [TIMM_COMUNS].[dbo].[TcomTiposCliente]
|  | LastUpdate | datetime | Timestamp of the last record modification. |
|  | LastUserID | int | System user ID who performed the last update. | References [TIMM_ADMIN].[dbo].[AdminAccount]
|  | AgenciaFilialID | numeric(18,0) | Branch or store ID where the customer was registered. |
|  | rowguid | uniqueidentifier | Unique ROWGUID for replication/sync purposes. |
|  | IDSexo | smallint | Gender identifier. | References [TIMM_COMUNS].[dbo].[TcomSexos]
|  | IDRate | int | **Foreign Key** Service Rating ID [Bronze, Platinum, ...].| References dbo.TbCrmClientRate  
|  | Status | bit | Current service status (e.g., 0=Active, 9=Deleted/Inactive). |
|  | DataNascimento | datetime | Date of birth. |
|  | LocalDeNascimento | varchar(100) | Place of birth (City/Region). | 
|  | ProfissaoID | int | Occupation/Profession code. | References [TIMM_COMUNS].[dbo].[Profissoes]
|  | CountryOfOriginID | int | Country ID for origin/nationality. |
|  | Nacionality | varchar(150) | Nationality description. |
|  | Registration | tinyint | Registration status. |
|  | Data1 | varchar(max) | Extended attribute field 1 (Generic). |
|  | Data2 | varchar(max) | Extended attribute field 2 (Generic). |
|  | Data3 | varchar(max) | Extended attribute field 3 (Generic). |
|  | Data4 | varchar(max) | Extended attribute field 4 (Generic). |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

