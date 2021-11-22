#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > crm.tbccClientes

# ![Tables](../../../../Images/Table32.png) [crm].[tbccClientes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ClienteID | numeric(18,0) | 9 | NOT NULL |
| Registration | tinyint | 1 | NULL allowed |
| NomeCompleto | varchar(200) | 200 | NOT NULL |
| NbrIdentidade | varchar(20) | 20 | NULL allowed |
| DataNascimento | datetime | 8 | NULL allowed |
| CountryOfOriginID | int | 4 | NULL allowed |
| Nacionality | varchar(150) | 150 | NULL allowed |
| ClienteIDUpper | numeric(18,0) | 9 | NULL allowed |
| TipoIdentidade | tinyint | 1 | NULL allowed |
| IDSexo | smallint | 2 | NULL allowed |
| TipoCliente | tinyint | 1 | NOT NULL |
| Data1 | varchar(max) | max | NULL allowed |
| Data2 | varchar(max) | max | NULL allowed |
| Data3 | varchar(max) | max | NULL allowed |
| Data4 | varchar(max) | max | NULL allowed |


---

## <a name="#uses"></a>Uses

* [crm]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

