#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.Timm_Servicos

# ![Tables](../../../../Images/Table32.png) [dbo].[Timm_Servicos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Description | References |
|---|---|---|---|---|
| [![Cluster Primary Key](../../../../Images/pkcluster.png)](#indexes) | ServicoID | numeric(18,0) | **Primary Key**. Unique identifier for the service. |
|  | MSISDN | varchar(50) | Mobile Station International Subscriber Directory Number (Phone Number). |
|  | ContaID | numeric(18,0) |**Foreign Key**. Identifier of the customer account owner. References dbo.TbccContas |
|  | ContratoID | numeric(18,0) | **Foreign Key** Identifier of the specific contract associated with this service. |
|  | ProfilePlanID | int | ID of the tariff plan or service profile assigned to this subscription. |
|  | DataAltProfile | datetime | Date when the profile/plan was last altered. |
|  | TipoServico | tinyint | Service type indicator (e.g., 21 - Mobile GSM, 25 - Broad Band). | References dbo.TcomTipoServico 
|  | DataCriacao | datetime | Timestamp when this service record was created. |
|  | PrimeiroUsoEm | datetime | Date of first usage/activation. |
|  | Lingua | tinyint | Preferred language code for communication. | References [TIMM_COMUNS].[dbo].[TiposLinguas]
|  | MotivoID | tinyint | Reason code for the current status or last change. |
|  | CredMensalPPS | int | Monthly credit allowance (Prepaid/PPS). |
|  | CredMensalTIMM | int | Monthly credit allowance (TIMM internal/Bonus). |
|  | Status | tinyint | Current service status (e.g., 1=Active, ..., 9=Deleted/Inactive). |
|  | DataStatus | datetime | Date when the current `Status` was applied. |
|  | Lastupdate | datetime | Timestamp of the last record modification. |
|  | LastuserID | int | ID of the system user or process that performed the last update. | References [TIMM_ADMIN].[dbo].[AdminAccount]
|  | AgenciaFilialID | numeric(18,0) | ID of the branch or agency associated with the sale/service. |
|  | IDRate | int | **Foreign Key** Service Rating ID [Bronze, Platinum, ...].| References dbo.TbCrmClientRate 
|  | MainkeyParent | Parent key for hierarchical service structures (e.g., Master/Slave accounts). |
|  | Data1 | varchar(max) | Extended attribute field 1 (Generic storage). |
|  | Data2 | varchar(max) | Extended attribute field 1 (Generic storage). |
|  | Data3 | varchar(max) | Extended attribute field 1 (Generic storage). |
|  | Data4 | varchar(max) | Extended attribute field 1 (Generic storage). |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

