#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomBillFormatos

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomBillFormatos]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomBillFormatos: BillFormato](../../../../Images/pkcluster.png)](#indexes) | BillFormato | tinyint | 1 | NOT NULL |
|  | BillFormatoDesc | varchar(100) | 100 | NOT NULL |
|  | MeioDivulgacao | varchar(20) | 20 | NULL allowed |
|  | FacturaDetalhada | tinyint | 1 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

