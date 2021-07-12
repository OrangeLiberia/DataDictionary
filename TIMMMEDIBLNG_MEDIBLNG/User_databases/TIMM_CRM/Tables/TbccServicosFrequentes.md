#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccServicosFrequentes

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccServicosFrequentes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccServicosFrequentes: Servico_ID\Mainkey](../../../../Images/pkcluster.png)](#indexes) | Servico_ID | decimal(18,0) | 9 | NOT NULL |
| [![Cluster Primary Key PK_TbccServicosFrequentes: Servico_ID\Mainkey](../../../../Images/pkcluster.png)](#indexes) | Mainkey | varchar(50) | 50 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | AgenciaFilialID | numeric(18,0) | 9 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

