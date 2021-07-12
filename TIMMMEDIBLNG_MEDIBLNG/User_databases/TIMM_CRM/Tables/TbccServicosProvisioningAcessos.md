#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccServicosProvisioningAcessos

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccServicosProvisioningAcessos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccServicosProvisioningAcessos: ServicoID\IDAcesso\IDCentral](../../../../Images/pkcluster.png)](#indexes) | ServicoID | numeric(18,0) | 9 | NOT NULL |
| [![Cluster Primary Key PK_TbccServicosProvisioningAcessos: ServicoID\IDAcesso\IDCentral](../../../../Images/pkcluster.png)](#indexes) | IDAcesso | int | 4 | NOT NULL |
|  | CentralFamilia | varchar(3) | 3 | NOT NULL |
| [![Cluster Primary Key PK_TbccServicosProvisioningAcessos: ServicoID\IDAcesso\IDCentral](../../../../Images/pkcluster.png)](#indexes) | IDCentral | int | 4 | NOT NULL |
|  | Mainkey | varchar(50) | 50 | NOT NULL |
|  | ESN | varchar(50) | 50 | NULL allowed |
|  | AcessoDataAct | datetime | 8 | NOT NULL |
|  | IDAcessoRestricao | int | 4 | NULL allowed |
|  | AcessoRestricaoDataAct | datetime | 8 | NULL allowed |
|  | AcessoRestricaoDataLim | datetime | 8 | NULL allowed |
|  | AcessoRestricaoOrigem | varchar(50) | 50 | NULL allowed |
|  | DataCriacaoCentralProvisioning | datetime | 8 | NULL allowed |
|  | DataRemoveCentralProvisioning | datetime | 8 | NULL allowed |
|  | AgenciaFilialID | int | 4 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | Default | tinyint | 1 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

