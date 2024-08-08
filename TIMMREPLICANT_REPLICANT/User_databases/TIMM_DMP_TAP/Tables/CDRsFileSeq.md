#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.CDRsFileSeq

# ![Tables](../../../../Images/Table32.png) [dbo].[CDRsFileSeq]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Indexes IX_SearchSequence
ix_CDRsFileSeq_PLMNID_Status_PLMNIDHomeOperator_TipoAcordo](../../../../Images/Index.png)](#indexes)(2) | PLMNID | varchar(7) | 7 | NOT NULL |  |
| [![Indexes ix_CDRsFileSeq_PLMNID_Status_PLMNIDHomeOperator_TipoAcordo](../../../../Images/Index.png)](#indexes) | FileSeq | int | 4 | NOT NULL |  |
| [![Indexes IX_SearchSequence](../../../../Images/Index.png)](#indexes) | Data | datetime | 8 | NULL allowed |  |
| [![Indexes IX_SearchSequence
ix_CDRsFileSeq_PLMNID_Status_PLMNIDHomeOperator_TipoAcordo](../../../../Images/Index.png)](#indexes)(2) | Status | tinyint | 1 | NULL allowed | ((0)) |
|  | LastUpdate | datetime | 8 | NULL allowed |  |
|  | LastUserID | int | 4 | NULL allowed |  |
| [![Indexes IX_SearchSequence
ix_CDRsFileSeq_PLMNID_Status_PLMNIDHomeOperator_TipoAcordo](../../../../Images/Index.png)](#indexes)(2) | PLMNIDHomeOperator | varchar(7) | 7 | NULL allowed |  |
| [![Indexes IX_SearchSequence
ix_CDRsFileSeq_PLMNID_Status_PLMNIDHomeOperator_TipoAcordo](../../../../Images/Index.png)](#indexes)(2) | TipoAcordo | varchar(1) | 1 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

