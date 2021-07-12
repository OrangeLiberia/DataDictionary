#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccModoAcesso

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccModoAcesso]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccModoAcesso: IDModoAcesso](../../../../Images/pkcluster.png)](#indexes) | IDModoAcesso | int | 4 | NOT NULL | 1 - 1 | NO |
|  | ModoAcesso | varchar(50) | 50 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | LastUpdate | smalldatetime | 4 | NOT NULL |  |  |
|  | Status | tinyint | 1 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

