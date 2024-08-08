#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdOrigDestClassesTarifario

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdOrigDestClassesTarifario]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbmdOrigDestClassesTarifario: CodOrigem\CodDestino\IDBillingServiceType](../../../../Images/pkcluster.png)](#indexes) | CodOrigem | varchar(10) | 10 | NOT NULL |
| [![Cluster Primary Key PK_TbmdOrigDestClassesTarifario: CodOrigem\CodDestino\IDBillingServiceType](../../../../Images/pkcluster.png)](#indexes) | CodDestino | varchar(10) | 10 | NOT NULL |
|  | ClasseTarifario_Automatico | varchar(20) | 20 | NOT NULL |
|  | ClasseTarifario_Manual | varchar(10) | 10 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUserUpdate | datetime | 8 | NOT NULL |
| [![Cluster Primary Key PK_TbmdOrigDestClassesTarifario: CodOrigem\CodDestino\IDBillingServiceType](../../../../Images/pkcluster.png)](#indexes) | IDBillingServiceType | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

