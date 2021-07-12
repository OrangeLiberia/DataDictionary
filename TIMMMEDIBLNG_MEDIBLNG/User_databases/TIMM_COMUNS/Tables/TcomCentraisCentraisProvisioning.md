#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomCentraisCentraisProvisioning

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomCentraisCentraisProvisioning]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomCentraisCentraisProvisioning: IDCentral\CentralProvisioning](../../../../Images/pkcluster.png)](#indexes) | IDCentral | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TcomCentraisCentraisProvisioning: IDCentral\CentralProvisioning](../../../../Images/pkcluster.png)](#indexes) | CentralProvisioning | varchar(10) | 10 | NOT NULL |
|  | Descricao | varchar(100) | 100 | NULL allowed |
|  | OrdemImportancia | tinyint | 1 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

