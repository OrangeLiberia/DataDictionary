#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccContas

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccContas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Description | References |
|---|---|---|---|---|
| [![ Cluster PK](../../../../Images/pkcluster.png)](#indexes) | ContaID | numeric(18,0) | **Primary Key**. Unique identifier for the billing account. |
|  | ContaDesc | varchar(200) | Description or alias for the account (e.g., "Main Account"). |
| FK | AgenciaFilialID | numeric(10,0) | Branch/Agency ID owning the account. |
|  | BillCicloFact | tinyint | Billing cycle day or code. |
|  | BillCelula | tinyint | Billing cell/group for batch processing. |
|  | BillFormato | tinyint | Invoice format preference (e.g., PDF, Paper, Summary) |
| FK | ClienteEnderecoID | numeric(18,0) | Foreign Key linking to the billing address. |
|  | ClienteID | numeric(18,0) | **Foreign Key**. The customer who owns this account. | References [dbo].[TbccClientes]
|  | MotivoID | tinyint | Reason code for the current status or last change. |
| FK | BillMoeda | int | Currency ID for the invoice/billing (e.g., USD, LRD, EUR, ...).  |
|  | BillUltimaData | datetime | Date of the last generated bill |
|  | Status | tinyint | Account status (e.g., 1 = Active, 9 = Closed). |
|  | StatusData | datetime | Date when the current status changed. |
|  | ModoPagamento | tinyint | Payment method (e.g., Direct Debit, Cash, Mobile Money). |
|  | ZonaInterbancaria | varchar(20) | Banking zone code (SEPA, SWIFT region, etc). |
|  | ContaBanco | varchar(50) | Bank Account Number. |
|  | NIB | varchar(50) | International Bank Account Number (IBAN/NIB). |
|  | ValMaxTB | decimal(18,0) |  Maximum credit limit or threshold. |
|  | Imposto | tinyint | Tax/VAT category code.  |
|  | PrazoPagamento | smallint | Payment terms in days (e.g., 30, 60). |
|  | DataCriacao | datetime | Account creation timestamp.  |
|  | DesactCicloLimit | tinyint | Limit cycle for deactivation logic. |
|  | PlafondCred | decimal(18,0) |  Credit ceiling/limit. |
|  | CustoVendaInd | tinyint | Cost indicator. |
|  | CentroCustoID | decimal(18,0) | Cost Center ID for corporate accounting. |
|  | CC1 | varchar(6) | Cost Center dimensions/levels 1 |
|  | CC2 | varchar(6) | Cost Center dimensions/levels 2 |
|  | CC3 | varchar(6) | Cost Center dimensions/levels 3 |
|  | CC4 | varchar(6) | Cost Center dimensions/levels 4 |
|  | CC5 | varchar(6) | Cost Center dimensions/levels 5 |
|  | TipoServico | tinyint | Service type classification. |
|  | EscCredTrabID | varchar(10) | Credit scale or work ID. |
|  | DataAtribCredTrab | datetime | Date credit attributes were assigned. |
|  | LastUserID | int | User ID of last modifier. |
|  | LastUpdate | datetime | Timestamp of last modification. |
|  | MoedaConta | int | Account currency  (e.g., USD, LRD, EUR, ...). |
|  | GestorContaID | int | Account Manager ID. |
|  | rowguid | uniqueidentifier | Unique ROWGUID for replication. |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

