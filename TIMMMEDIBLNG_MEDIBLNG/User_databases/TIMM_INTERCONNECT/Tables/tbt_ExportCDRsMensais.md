#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_ExportCDRsMensais

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_ExportCDRsMensais]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_ExportCDRsMensais: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | IDVolumeMensal | int | 4 | NULL allowed |  |
|  | XML_Statment | xml | max | NULL allowed |  |
|  | lastuserupdate | int | 4 | NULL allowed |  |
|  | lastdateupdate | datetime | 8 | NULL allowed |  |
|  | createddate | datetime | 8 | NULL allowed |  |
|  | Status | varchar(max) | max | NULL allowed |  |
|  | tipotrafego_id | tinyint | 1 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

