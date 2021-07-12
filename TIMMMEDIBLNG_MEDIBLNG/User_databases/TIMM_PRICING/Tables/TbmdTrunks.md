#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdTrunks

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdTrunks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tbmdTrunks: Trunk\EntradaSaida\IDCentral](../../../../Images/pkcluster.png)](#indexes) | Trunk | varchar(50) | 50 | NOT NULL |
|  | Description | varchar(250) | 250 | NOT NULL |
|  | DataRegsito | datetime | 8 | NOT NULL |
|  | IDAccount | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_tbmdTrunks: Trunk\EntradaSaida\IDCentral](../../../../Images/pkcluster.png)](#indexes) | EntradaSaida | char(1) | 1 | NOT NULL |
| [![Cluster Primary Key PK_tbmdTrunks: Trunk\EntradaSaida\IDCentral](../../../../Images/pkcluster.png)](#indexes) | IDCentral | varchar(50) | 50 | NOT NULL |
|  | Operador | varchar(50) | 50 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

