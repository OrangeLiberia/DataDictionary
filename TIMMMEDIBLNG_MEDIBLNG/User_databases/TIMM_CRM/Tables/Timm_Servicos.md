#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.Timm_Servicos

# ![Tables](../../../../Images/Table32.png) [dbo].[Timm_Servicos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tbcrmServicos_Servico_ID: ServicoID](../../../../Images/pkcluster.png)](#indexes) | ServicoID | numeric(18,0) | 9 | NOT NULL |
|  | MSISDN | varchar(50) | 50 | NOT NULL |
|  | ContaID | numeric(18,0) | 9 | NOT NULL |
|  | ContratoID | numeric(18,0) | 9 | NULL allowed |
|  | ProfilePlanID | int | 4 | NULL allowed |
|  | DataAltProfile | datetime | 8 | NULL allowed |
|  | TipoServico | tinyint | 1 | NOT NULL |
|  | DataCriacao | datetime | 8 | NOT NULL |
|  | PrimeiroUsoEm | datetime | 8 | NULL allowed |
|  | Lingua | tinyint | 1 | NULL allowed |
|  | MotivoID | tinyint | 1 | NULL allowed |
|  | CredMensalPPS | int | 4 | NULL allowed |
|  | CredMensalTIMM | int | 4 | NULL allowed |
|  | Status | tinyint | 1 | NOT NULL |
|  | DataStatus | datetime | 8 | NOT NULL |
|  | Lastupdate | datetime | 8 | NOT NULL |
|  | LastuserID | int | 4 | NOT NULL |
|  | AgenciaFilialID | numeric(18,0) | 9 | NULL allowed |
|  | IDRate | int | 4 | NULL allowed |
|  | MainkeyParent | bigint | 8 | NULL allowed |
|  | Data1 | varchar(max) | max | NULL allowed |
|  | Data2 | varchar(max) | max | NULL allowed |
|  | Data3 | varchar(max) | max | NULL allowed |
|  | Data4 | varchar(max) | max | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

