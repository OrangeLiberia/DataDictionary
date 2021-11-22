#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Documento_Factura

# ![Tables](../../../../Images/Table32.png) [dbo].[Documento_Factura]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Documento: Documento_ID](../../../../Images/pkcluster.png)](#indexes) | Documento_ID | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | Tipo_Estado | int | 4 | NULL allowed |  |  |
|  | Numero_Documento | varchar(50) | 50 | NOT NULL |  |  |
|  | Data_Documento | smalldatetime | 4 | NOT NULL |  |  |
|  | Data_Periodo_de | smalldatetime | 4 | NULL allowed |  |  |
|  | Data_Periodo_ate | smalldatetime | 4 | NULL allowed |  |  |
|  | Operadora_de_ID | int | 4 | NULL allowed |  |  |
|  | Operadora_Nome_de | varchar(200) | 200 | NULL allowed |  |  |
|  | Morada_de | varchar(500) | 500 | NULL allowed |  |  |
|  | Localidade_de | varchar(100) | 100 | NULL allowed |  |  |
|  | Zip_Code_de | varchar(15) | 15 | NULL allowed |  |  |
|  | NIPC_de | varchar(50) | 50 | NULL allowed |  |  |
|  | Operadora_para_ID | int | 4 | NULL allowed |  |  |
|  | Operadora_Nome_para | varchar(200) | 200 | NULL allowed |  |  |
|  | Morada_para | varchar(500) | 500 | NULL allowed |  |  |
|  | Localidade_para | varchar(100) | 100 | NULL allowed |  |  |
|  | Zip_Code_para | varchar(15) | 15 | NULL allowed |  |  |
|  | NIPC_para | varchar(50) | 50 | NULL allowed |  |  |
|  | Tipo_Doc | varchar(3) | 3 | NOT NULL |  |  |
|  | TAX_VAT_Descricao | varchar(50) | 50 | NULL allowed |  |  |
|  | TAX_VAT_Value | float | 8 | NULL allowed |  |  |
|  | TAX_VAT_Amount | float | 8 | NULL allowed |  |  |
|  | Amount | numeric(18,6) | 9 | NULL allowed |  |  |
|  | Total_Call | float | 8 | NULL allowed |  |  |
|  | Total_Minutes | float | 8 | NULL allowed |  |  |
|  | Currency | varchar(50) | 50 | NULL allowed |  |  |
|  | Parent_ID | bigint | 8 | NULL allowed |  |  |
|  | Hubbing | tinyint | 1 | NULL allowed |  | ((0)) |
|  | Data_Criacao | smalldatetime | 4 | NOT NULL |  |  |
|  | User_ID | int | 4 | NOT NULL |  |  |
|  | Factura | varchar(50) | 50 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

