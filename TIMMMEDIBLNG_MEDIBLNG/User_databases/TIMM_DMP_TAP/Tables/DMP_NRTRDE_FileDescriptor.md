#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_NRTRDE_FileDescriptor

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_NRTRDE_FileDescriptor]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_NRTRDE_FileDescriptor: FileID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_ProcessDateFileName](../../../../Images/Index.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Indexes IX_ProcessDateFileName](../../../../Images/Index.png)](#indexes) | FileName | varchar(200) | 200 | NOT NULL |  |
|  | Path | varchar(500) | 500 | NOT NULL |  |
|  | CommitCharge | int | 4 | NULL allowed |  |
| [![Indexes IX_ProcessDateFileName](../../../../Images/Index.png)](#indexes) | ProcessingStart | datetime | 8 | NULL allowed |  |
|  | ProcessingEnd | datetime | 8 | NOT NULL | (getdate()) |
|  | FirstCDRTime | datetime | 8 | NULL allowed |  |
|  | LastCDRTime | datetime | 8 | NULL allowed |  |
|  | MocCount | int | 4 | NULL allowed | ((0)) |
|  | MtcCount | int | 4 | NULL allowed | ((0)) |
|  | GprsCount | int | 4 | NULL allowed | ((0)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

