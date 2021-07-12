#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_NRTRDE_FileDescriptor_OUT

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_NRTRDE_FileDescriptor_OUT]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_NRTRDE_FileDescriptor_OUT: FileID\IDOperator](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_GPRSIdOperatorWrkGID](../../../../Images/Index.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Indexes IX_MOC](../../../../Images/Index.png)](#indexes) | MOC | bit | 1 | NOT NULL | ((0)) |
| [![Indexes IX_MTC](../../../../Images/Index.png)](#indexes) | MTC | bit | 1 | NOT NULL | ((0)) |
| [![Indexes IX_SMO](../../../../Images/Index.png)](#indexes) | SMO | bit | 1 | NOT NULL | ((0)) |
| [![Indexes IX_SMT](../../../../Images/Index.png)](#indexes) | SMT | bit | 1 | NOT NULL | ((0)) |
| [![Indexes IX_GPRS
IX_GPRSIdOperatorWrkGID](../../../../Images/Index.png)](#indexes)(2) | GPRS | bit | 1 | NOT NULL | ((0)) |
| [![Cluster Primary Key PK_DMP_NRTRDE_FileDescriptor_OUT: FileID\IDOperator](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_GPRSIdOperatorWrkGID](../../../../Images/Index.png)](#indexes) | IDOperator | bigint | 8 | NOT NULL |  |
| [![Indexes IX_GPRSIdOperatorWrkGID](../../../../Images/Index.png)](#indexes) | WorkGroupID | bigint | 8 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

