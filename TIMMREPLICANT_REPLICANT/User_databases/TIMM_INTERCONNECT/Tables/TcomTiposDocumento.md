#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.TcomTiposDocumento

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomTiposDocumento]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomTiposDocumento: Tipo_Doc](../../../../Images/pkcluster.png)](#indexes) | Tipo_Doc | varchar(3) | 3 | NOT NULL |  |
|  | Descricao | varchar(20) | 20 | NOT NULL |  |
|  | Deb_Cred | tinyint | 1 | NOT NULL |  |
|  | Tipo_Doc_Anul | varchar(3) | 3 | NULL allowed |  |
|  | Sinal | tinyint | 1 | NULL allowed |  |
|  | TipoDocNum | tinyint | 1 | NULL allowed |  |
|  | TipoDocCorrNeg | varchar(3) | 3 | NULL allowed |  |
|  | TipoDocCorrPos | varchar(3) | 3 | NULL allowed |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL | (newid()) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

