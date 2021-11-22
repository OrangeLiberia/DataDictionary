#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomTiposCliente

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomTiposCliente]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomTiposCliente: TipoCliente](../../../../Images/pkcluster.png)](#indexes) | TipoCliente | tinyint | 1 | NOT NULL |
|  | TipoClienteDesc | varchar(100) | 100 | NOT NULL |
|  | BillMoeda | numeric(10,0) | 9 | NOT NULL |
|  | CustoVendaInd | tinyint | 1 | NOT NULL |
|  | EscTrabCred | tinyint | 1 | NULL allowed |
|  | IDTipoImposto | int | 4 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | GrupoTipoCliente | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

