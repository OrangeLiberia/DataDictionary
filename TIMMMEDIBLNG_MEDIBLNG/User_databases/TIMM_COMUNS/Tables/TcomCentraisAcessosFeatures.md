#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomCentraisAcessosFeatures

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomCentraisAcessosFeatures]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TNet_BusinessCenarios_TC: IDAcessoFeature](../../../../Images/pkcluster.png)](#indexes) | IDAcessoFeature | int | 4 | NOT NULL |
|  | CentralFamilia | varchar(3) | 3 | NOT NULL |
|  | Descricao | varchar(300) | 300 | NOT NULL |
|  | Grupo | tinyint | 1 | NULL allowed |
|  | Nivel | tinyint | 1 | NULL allowed |
|  | Categoria | tinyint | 1 | NOT NULL |
|  | DefaultCriarNaCentral | bit | 1 | NOT NULL |
|  | Activo | bit | 1 | NOT NULL |
|  | StatusPos | smallint | 2 | NULL allowed |
|  | StatusPre | smallint | 2 | NULL allowed |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | PermissionID | bigint | 8 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

