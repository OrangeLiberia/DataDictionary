#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.tbccProfilePlansCUGs

# ![Tables](../../../../Images/Table32.png) [dbo].[tbccProfilePlansCUGs]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbccProfilePlansCUGs: ProfilePlansCUGsID](../../../../Images/pkcluster.png)](#indexes) | ProfilePlansCUGsID | int | 4 | NOT NULL | 1 - 1 | NO |
|  | NumMin | int | 4 | NOT NULL |  |  |
|  | NumMax | int | 4 | NOT NULL |  |  |
|  | Status | tinyint | 1 | NOT NULL |  |  |
|  | Controlo | bit | 1 | NOT NULL |  |  |
|  | CompartilhaFranquia | bit | 1 | NOT NULL |  |  |
|  | CUGZero | bit | 1 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

