#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_ReprocessMensalStatus

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_ReprocessMensalStatus]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_Reprocessa: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | IDVolumeMensal | int | 4 | NULL allowed |  |  |
|  | lastuserupdate | int | 4 | NULL allowed |  |  |
|  | lastdateupdate | datetime | 8 | NULL allowed |  |  |
|  | createddate | datetime | 8 | NULL allowed |  |  |
|  | Status | varchar(max) | max | NULL allowed |  | ('ICON.REPROCESSAMENTO.CLEAN') |
|  | OrigemReprocessamento | varchar(max) | max | NULL allowed |  |  |
|  | DadosReprocessa | int | 4 | NULL allowed |  | ((1)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

