#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.tbccPlanoAbonosDescontos

# ![Tables](../../../../Images/Table32.png) [dbo].[tbccPlanoAbonosDescontos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbccPlanoAbonosDescontos: IDPlanoAD](../../../../Images/pkcluster.png)](#indexes) | IDPlanoAD | int | 4 | NOT NULL | 1 - 1 | NO |
|  | Designacao | varchar(50) | 50 | NOT NULL |  |  |
|  | DiaInicioDebito | tinyint | 1 | NOT NULL |  |  |
|  | Status | tinyint | 1 | NOT NULL |  |  |
|  | LastUpdate | smalldatetime | 4 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |
|  | DebtCred | tinyint | 1 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

