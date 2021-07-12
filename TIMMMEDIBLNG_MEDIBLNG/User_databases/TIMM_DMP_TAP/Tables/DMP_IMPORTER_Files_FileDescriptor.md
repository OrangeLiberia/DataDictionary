#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_IMPORTER_Files_FileDescriptor

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_IMPORTER_Files_FileDescriptor]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_IMPORTER_Files_FileDescriptor: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | VersionNumber | varchar(4) | 4 | NULL allowed |  |  |
|  | TipoAcordo | varchar(1) | 1 | NULL allowed |  |  |
|  | sender | varchar(50) | 50 | NULL allowed |  |  |
|  | recipient | varchar(50) | 50 | NULL allowed |  |  |
|  | localCurrency | varchar(50) | 50 | NULL allowed |  |  |
|  | exchangeRate | numeric(18,5) | 9 | NULL allowed |  |  |
|  | totalCharge | numeric(18,5) | 9 | NULL allowed |  |  |
|  | totalTaxValue | numeric(18,5) | 9 | NULL allowed |  |  |
|  | totalDiscountValue | numeric(18,5) | 9 | NULL allowed |  |  |
|  | callEventDetailsCount | bigint | 8 | NULL allowed |  |  |
| [![Indexes IX_ASNNAme](../../../../Images/Index.png)](#indexes) | ASNInputName | varchar(256) | 256 | NULL allowed |  |  |
|  | ASNInputFolder | varchar(256) | 256 | NULL allowed |  |  |
|  | XMLName | varchar(256) | 256 | NULL allowed |  |  |
|  | XMLOutputFolder | varchar(256) | 256 | NULL allowed |  |  |
|  | ASNName | varchar(256) | 256 | NULL allowed |  |  |
|  | ASNOutputFolder | varchar(256) | 256 | NULL allowed |  |  |
| [![Indexes IX_ProcessDate](../../../../Images/Index.png)](#indexes) | ProcessDate | datetime | 8 | NULL allowed |  |  |
|  | MocCount | int | 4 | NULL allowed |  | ((0)) |
|  | MtcCount | int | 4 | NULL allowed |  | ((0)) |
|  | GPRSCount | int | 4 | NULL allowed |  | ((0)) |
|  | SMSTCount | int | 4 | NULL allowed |  | ((0)) |
|  | SMSOCount | int | 4 | NULL allowed |  | ((0)) |
|  | ProcessedBilling | int | 4 | NULL allowed |  | ((0)) |
|  | ProcessedRoaming | int | 4 | NULL allowed |  | ((0)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

