#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.tbt_CDRDuplicate

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_CDRDuplicate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_CDRDuplicate: FK_FileDesc_ID\FileID\CDRID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | FK_FileDesc_ID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_tbt_CDRDuplicate: FK_FileDesc_ID\FileID\CDRID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_tbt_CDRDuplicate: FK_FileDesc_ID\FileID\CDRID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_tbt_CDRDuplicate: FK_FileDesc_ID\FileID\CDRID\FK_Central_ID](../../../../Images/pkcluster.png)](#indexes) | FK_Central_ID | int | 4 | NOT NULL |
| [![Indexes IX_NumeroData](../../../../Images/Index.png)](#indexes) | numeroData | nvarchar(250) | 500 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

