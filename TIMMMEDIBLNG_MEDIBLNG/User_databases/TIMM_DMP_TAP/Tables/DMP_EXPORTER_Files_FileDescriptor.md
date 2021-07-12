#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_EXPORTER_Files_FileDescriptor

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_EXPORTER_Files_FileDescriptor]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_EXPORTER_Files_FileDescriptor_1: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | SpecificDay | datetime | 8 | NULL allowed |  |  |
|  | PLMNID | varchar(6) | 6 | NULL allowed |  |  |
|  | XMLName | varchar(256) | 256 | NULL allowed |  |  |
|  | XMLOutputFolder | varchar(256) | 256 | NULL allowed |  |  |
| [![Indexes ix_DMP_EXPORTER_Files_FileDescriptor_ASNName_ProcessDate](../../../../Images/Index.png)](#indexes) | ASNName | varchar(256) | 256 | NULL allowed |  |  |
|  | ASNOutputFolder | varchar(256) | 256 | NULL allowed |  |  |
| [![Indexes ix_DMP_EXPORTER_Files_FileDescriptor_ASNName_ProcessDate](../../../../Images/Index.png)](#indexes) | ProcessDate | datetime | 8 | NULL allowed |  |  |
|  | FileSeq | int | 4 | NULL allowed |  |  |
|  | MocCount | int | 4 | NULL allowed |  | ((0)) |
|  | MtcCount | int | 4 | NULL allowed |  | ((0)) |
|  | GPRSCount | int | 4 | NULL allowed |  | ((0)) |
|  | PLMNIDHomeOperator | varchar(7) | 7 | NULL allowed |  |  |
|  | SmsoCount | int | 4 | NULL allowed |  |  |
|  | TipoAcordo | varchar(1) | 1 | NULL allowed |  |  |
|  | SmstCount | int | 4 | NULL allowed |  | ((0)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

