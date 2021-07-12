#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_ReprocessTrunksStatus

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_ReprocessTrunksStatus]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_ReprocessTrunksStatus: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | IDVolumeMensal | int | 4 | NULL allowed |  |  |
|  | trunkID | int | 4 | NULL allowed |  |  |
|  | FK_Central_ID | int | 4 | NULL allowed |  |  |
|  | lastuserupdate | int | 4 | NULL allowed |  |  |
|  | lastdateupdate | datetime | 8 | NULL allowed |  |  |
|  | createddate | datetime | 8 | NULL allowed |  |  |
|  | Status | varchar(max) | max | NULL allowed |  | ('ICON.REP.TRUNK.TOREPROCESS') |
|  | DadosReprocessa | int | 4 | NULL allowed |  | ((1)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

