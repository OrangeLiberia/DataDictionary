#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_AgreementDefinition

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_AgreementDefinition]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| ID | int | 4 | NOT NULL | 1 - 1 |
| IDAgreement | int | 4 | NULL allowed |  |
| Direction | tinyint | 1 | NULL allowed |  |
| FlowID | int | 4 | NULL allowed |  |
| CallOri | int | 4 | NULL allowed |  |
| CallDest | int | 4 | NULL allowed |  |
| Price | numeric(18,6) | 9 | NULL allowed |  |
| LowerLimit | int | 4 | NULL allowed |  |
| HigherLimit | int | 4 | NULL allowed |  |
| StartHour | varchar(50) | 50 | NULL allowed |  |
| EndHour | varchar(50) | 50 | NULL allowed |  |
| Description | varchar(max) | max | NULL allowed |  |
| IDHubbing | int | 4 | NULL allowed |  |
| TipoRateID | int | 4 | NULL allowed |  |
| TipoServicoID | int | 4 | NULL allowed |  |
| CO_IDC_OTTrafegoDefinition | int | 4 | NULL allowed |  |
| CD_IDC_OTTrafegoDefinition | int | 4 | NULL allowed |  |
| GroupID | int | 4 | NULL allowed |  |
| TipoPercentagemID | int | 4 | NULL allowed |  |
| Percentagem | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

