#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Views](Views.md) > dbo.v_CurrencyConversion_TiposMoedas

# ![Views](../../../../Images/View32.png) [dbo].[v_CurrencyConversion_TiposMoedas]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| id_origem | int | 4 |
| cod origem | varchar(12) | 12 |
| desig origem | varchar(50) | 50 |
| abrev origem | varchar(20) | 20 |
| id_destino | int | 4 |
| cod destino | varchar(12) | 12 |
| desig destino | varchar(50) | 50 |
| abrev destino | varchar(20) | 20 |
| datainicio | datetime | 8 |
| datafim | datetime | 8 |
| taxa | numeric(38,19) | 17 |
| lastupdate | datetime | 8 |
| lastuserid | int | 4 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

