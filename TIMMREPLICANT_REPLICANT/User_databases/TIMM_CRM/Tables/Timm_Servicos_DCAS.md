#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.Timm_Servicos_DCAS

# ![Tables](../../../../Images/Table32.png) [dbo].[Timm_Servicos_DCAS]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
|  | ID | int | 4 | NOT NULL | 1 - 1 | NO |
| [![Cluster Primary Key PK_Timm_Servicos_DCAS: ServicoID](../../../../Images/pkcluster.png)](#indexes) | ServicoID | numeric(18,0) | 9 | NOT NULL |  |  |
|  | BeginDate | datetime | 8 | NULL allowed |  |  |
|  | EndDate | datetime | 8 | NULL allowed |  |  |
|  | Status | tinyint | 1 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NULL allowed |  |  |
|  | Created_At | datetime | 8 | NOT NULL |  |  |
|  | Updated_At | datetime | 8 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

