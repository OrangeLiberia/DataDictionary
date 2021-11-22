#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Linha_Documento

# ![Tables](../../../../Images/Table32.png) [dbo].[Linha_Documento]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Linha_Documento: Linha_Documento_ID](../../../../Images/pkcluster.png)](#indexes) | Linha_Documento_ID | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | Documento_ID | bigint | 8 | NOT NULL |  |  |
|  | Data_Periodo | smalldatetime | 4 | NOT NULL |  |  |
|  | Origem | varchar(200) | 200 | NULL allowed |  |  |
|  | Transit | varchar(200) | 200 | NULL allowed |  |  |
|  | Destination | varchar(200) | 200 | NULL allowed |  |  |
|  | Descritivo | varchar(max) | max | NULL allowed |  |  |
|  | Class | varchar(50) | 50 | NULL allowed |  |  |
|  | Tariff | varchar(50) | 50 | NULL allowed |  |  |
|  | Num_Call | float | 8 | NOT NULL |  |  |
|  | Minutes | float | 8 | NOT NULL |  |  |
|  | Currency | varchar(50) | 50 | NOT NULL |  |  |
|  | TAX_VAT_Descricao | varchar(150) | 150 | NOT NULL |  |  |
|  | TAX_VAT_Value | float | 8 | NOT NULL |  |  |
|  | TAX_VAT_Amount | float | 8 | NOT NULL |  |  |
|  | Minutes_Rate | numeric(18,6) | 9 | NULL allowed |  |  |
|  | Amount | numeric(18,6) | 9 | NULL allowed |  |  |
|  | Data_Criacao | smalldatetime | 4 | NOT NULL |  | (getdate()) |
|  | User_ID | int | 4 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

