#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomCentraisRanges

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomCentraisRanges]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomCentraisRanges: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 | NO |
|  | IDCentral | int | 4 | NOT NULL |  |  |
|  | Designacao | varchar(200) | 200 | NOT NULL |  |  |
|  | IDAreaCode | int | 4 | NOT NULL |  |  |
|  | CentralCode | int | 4 | NOT NULL |  |  |
|  | LowerRange | bigint | 8 | NOT NULL |  |  |
|  | UpperRange | bigint | 8 | NOT NULL |  |  |
|  | InstalledCapacity | int | 4 | NULL allowed |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

