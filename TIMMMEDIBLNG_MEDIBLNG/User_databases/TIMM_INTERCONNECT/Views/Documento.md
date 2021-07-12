#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Views](Views.md) > dbo.Documento

# ![Views](../../../../Images/View32.png) [dbo].[Documento]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Documento_ID | bigint | 8 | 0 - 0 |
| Tipo_Estado | int | 4 |  |
| Numero_Documento | varchar(50) | 50 |  |
| Data_Documento | smalldatetime | 4 |  |
| Data_Periodo_de | smalldatetime | 4 |  |
| Data_Periodo_ate | smalldatetime | 4 |  |
| Operadora_de_ID | int | 4 |  |
| Operadora_Nome_de | varchar(200) | 200 |  |
| Morada_de | varchar(500) | 500 |  |
| Localidade_de | varchar(100) | 100 |  |
| Zip_Code_de | varchar(15) | 15 |  |
| NIPC_de | varchar(50) | 50 |  |
| Operadora_para_ID | int | 4 |  |
| Operadora_Nome_para | varchar(200) | 200 |  |
| Morada_para | varchar(500) | 500 |  |
| Localidade_para | varchar(100) | 100 |  |
| Zip_Code_para | varchar(15) | 15 |  |
| NIPC_para | varchar(50) | 50 |  |
| Tipo_Doc | varchar(3) | 3 |  |
| TAX_VAT_Descricao | varchar(50) | 50 |  |
| TAX_VAT_Value | float | 8 |  |
| TAX_VAT_Amount | float | 8 |  |
| Amount | numeric(18,6) | 9 |  |
| Total_Call | float | 8 |  |
| Total_Minutes | float | 8 |  |
| Currency | varchar(50) | 50 |  |
| Parent_ID | bigint | 8 |  |
| Data_Criacao | smalldatetime | 4 |  |
| User_ID | int | 4 |  |
| Hubbing | tinyint | 1 |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

