#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccServicosProvisioningFeatures

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccServicosProvisioningFeatures]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccServicosProvisioningFeatures: ServicoID\IDFeature\IDCentral](../../../../Images/pkcluster.png)](#indexes) | ServicoID | numeric(18,0) | 9 | NOT NULL |
| [![Cluster Primary Key PK_TbccServicosProvisioningFeatures: ServicoID\IDFeature\IDCentral](../../../../Images/pkcluster.png)](#indexes) | IDFeature | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccServicosProvisioningFeatures: ServicoID\IDFeature\IDCentral](../../../../Images/pkcluster.png)](#indexes) | IDCentral | int | 4 | NOT NULL |
|  | CentralFamilia | varchar(3) | 3 | NOT NULL |
|  | Mainkey | varchar(50) | 50 | NOT NULL |
|  | ESN | varchar(50) | 50 | NULL allowed |
|  | Status | tinyint | 1 | NOT NULL |
|  | AgenciaFilialID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | Default | tinyint | 1 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

