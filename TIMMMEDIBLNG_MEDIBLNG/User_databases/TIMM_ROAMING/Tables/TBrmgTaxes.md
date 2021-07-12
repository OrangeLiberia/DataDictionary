#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgTaxes

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgTaxes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Indexes IX_TBrmgTaxes](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Cluster Primary Key PK_TBrmgTaxes: KeyTax](../../../../Images/pkcluster.png)](#indexes) | KeyTax | varchar(50) | 50 | NOT NULL |  |  |
|  | Descricao | varchar(500) | 500 | NOT NULL |  |  |
|  | Valor | decimal(7,7) | 5 | NOT NULL |  |  |
|  | taxTypeID | varchar(2) | 2 | NULL allowed |  |  |
|  | KeyCodeLang | varchar(50) | 50 | NULL allowed |  |  |
|  | lastuserid | int | 4 | NOT NULL |  | ((0)) |
|  | lastupdate | datetime | 8 | NOT NULL |  | (getdate()) |
|  | Status | bit | 1 | NOT NULL |  | ((1)) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

