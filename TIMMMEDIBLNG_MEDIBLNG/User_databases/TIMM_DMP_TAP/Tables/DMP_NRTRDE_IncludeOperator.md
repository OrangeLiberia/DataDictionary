#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_NRTRDE_IncludeOperator

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_NRTRDE_IncludeOperator]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_NRTRDE_IncludeOperator: IDHomeOperator\IDOperator](../../../../Images/pkcluster.png)](#indexes) | IDHomeOperator | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_DMP_NRTRDE_IncludeOperator: IDHomeOperator\IDOperator](../../../../Images/pkcluster.png)](#indexes) | IDOperator | bigint | 8 | NOT NULL |  |
|  | FileSequence | bigint | 8 | NOT NULL | ((0)) |
|  | Enabled | bit | 1 | NOT NULL | ((0)) |
|  | ConfigType | varchar(50) | 50 | NOT NULL | ('SINGLE') |
|  | DateBegin | datetime | 8 | NOT NULL | (getdate()) |
|  | DateEnd | datetime | 8 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

