#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomCentrais

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomCentrais]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomCentrais: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 | NO |
|  | IDModelo | int | 4 | NOT NULL |  |  |
|  | Designacao | varchar(50) | 50 | NOT NULL |  |  |
|  | Abreviatura | varchar(50) | 50 | NOT NULL |  |  |
|  | CentralFamilia | varchar(3) | 3 | NOT NULL |  |  |
|  | Activo | bit | 1 | NOT NULL |  |  |
|  | AgenciaFilialID | int | 4 | NOT NULL |  |  |
|  | IDCentral_CDR | varchar(50) | 50 | NULL allowed |  |  |
|  | TipoServico | int | 4 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

