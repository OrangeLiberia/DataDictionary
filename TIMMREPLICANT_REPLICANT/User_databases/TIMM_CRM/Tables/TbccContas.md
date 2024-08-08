#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccContas

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccContas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccContas_ContaID: ContaID](../../../../Images/pkcluster.png)](#indexes) | ContaID | numeric(18,0) | 9 | NOT NULL |
|  | ContaDesc | varchar(200) | 200 | NOT NULL |
|  | AgenciaFilialID | numeric(10,0) | 9 | NOT NULL |
|  | BillCicloFact | tinyint | 1 | NOT NULL |
|  | BillCelula | tinyint | 1 | NOT NULL |
|  | BillFormato | tinyint | 1 | NOT NULL |
|  | ClienteEnderecoID | numeric(18,0) | 9 | NOT NULL |
|  | ClienteID | numeric(18,0) | 9 | NOT NULL |
|  | MotivoID | tinyint | 1 | NULL allowed |
|  | BillMoeda | int | 4 | NOT NULL |
|  | BillUltimaData | datetime | 8 | NULL allowed |
|  | Status | tinyint | 1 | NOT NULL |
|  | StatusData | datetime | 8 | NOT NULL |
|  | ModoPagamento | tinyint | 1 | NOT NULL |
|  | ZonaInterbancaria | varchar(20) | 20 | NULL allowed |
|  | ContaBanco | varchar(50) | 50 | NULL allowed |
|  | NIB | varchar(50) | 50 | NULL allowed |
|  | ValMaxTB | decimal(18,0) | 9 | NULL allowed |
|  | Imposto | tinyint | 1 | NULL allowed |
|  | PrazoPagamento | smallint | 2 | NULL allowed |
|  | DataCriacao | datetime | 8 | NOT NULL |
|  | DesactCicloLimit | tinyint | 1 | NULL allowed |
|  | PlafondCred | decimal(18,0) | 9 | NULL allowed |
|  | CustoVendaInd | tinyint | 1 | NOT NULL |
|  | CentroCustoID | decimal(18,0) | 9 | NULL allowed |
|  | CC1 | varchar(6) | 6 | NULL allowed |
|  | CC2 | varchar(6) | 6 | NULL allowed |
|  | CC3 | varchar(6) | 6 | NULL allowed |
|  | CC4 | varchar(6) | 6 | NULL allowed |
|  | CC5 | varchar(6) | 6 | NULL allowed |
|  | TipoServico | tinyint | 1 | NOT NULL |
|  | EscCredTrabID | varchar(10) | 10 | NULL allowed |
|  | DataAtribCredTrab | datetime | 8 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | MoedaConta | int | 4 | NULL allowed |
|  | GestorContaID | int | 4 | NULL allowed |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

