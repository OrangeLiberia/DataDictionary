#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.tbccCUGs

# ![Tables](../../../../Images/Table32.png) [dbo].[tbccCUGs]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbccCUGs: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 | NO |
|  | Nome | varchar(50) | 50 | NOT NULL |  |  |
|  | Descricao | varchar(200) | 200 | NOT NULL |  |  |
|  | MaxMembers | int | 4 | NOT NULL |  |  |
|  | PPSID | int | 4 | NOT NULL |  |  |
|  | Alocado | bit | 1 | NOT NULL |  |  |
|  | ClienteID | numeric(18,0) | 9 | NULL allowed |  |  |
|  | ProfilePlanID | int | 4 | NULL allowed |  |  |
|  | ContaID | numeric(18,0) | 9 | NULL allowed |  |  |
|  | LastUserID | char(10) | 10 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

