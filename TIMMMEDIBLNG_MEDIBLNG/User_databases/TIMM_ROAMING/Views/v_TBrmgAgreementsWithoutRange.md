#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Views](Views.md) > dbo.v_TBrmgAgreementsWithoutRange

# ![Views](../../../../Images/View32.png) [dbo].[v_TBrmgAgreementsWithoutRange]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Last Modified | 3:13:27 AM Tuesday, October 4, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Collation | Max Length (Bytes) |
|---|---|---|---|
| IDAgreement | bigint |  | 8 |
| AgreementName | varchar(200) | Latin1_General_CI_AS | 200 |
| IDHomeOperator | int |  | 4 |
| HomeOperatorName | varchar(150) | SQL_Latin1_General_CP1_CI_AS | 150 |
| AgreementType | varchar(10) | Latin1_General_CI_AS | 10 |
| Rating Type | varchar(200) | Latin1_General_CI_AS | 200 |
| ID Rating Type | varchar(20) | Latin1_General_CI_AS | 20 |
| IDOperator | int |  | 4 |
| OperatorName | varchar(150) | SQL_Latin1_General_CP1_CI_AS | 150 |
| PLMNIDOperator | varchar(10) | SQL_Latin1_General_CP1_CI_AS | 10 |
| IDParentOperator | int |  | 4 |
| ParentOperatorName | varchar(150) | SQL_Latin1_General_CP1_CI_AS | 150 |
| PLMNIDParentOperator | varchar(5) | Latin1_General_CI_AS | 5 |
| MCC | varchar(3) | SQL_Latin1_General_CP1_CI_AS | 3 |
| MNC | varchar(3) | SQL_Latin1_General_CP1_CI_AS | 3 |
| MCCMNC | varchar(6) | SQL_Latin1_General_CP1_CI_AS | 6 |
| AgreementStatusID | int |  | 4 |
| TipoAcordo | varchar(1) | Latin1_General_CI_AS | 1 |
| KeyStatus | varchar(50) | Latin1_General_CI_AS | 50 |
| DescricaoTipoAcordo | varchar(500) | Latin1_General_CI_AS | 500 |
| DateBegin | datetime |  | 8 |
| DateEnd | datetime |  | 8 |
| TaxesApplied | int |  | 4 |
| DescricaoTipoTax | varchar(500) | Latin1_General_CI_AS | 500 |
| TipoMoedaID | int |  | 4 |
| Cod_ID_Moeda | varchar(12) | SQL_Latin1_General_CP1_CI_AS | 12 |
| Desig_Completa | varchar(50) | SQL_Latin1_General_CP1_CI_AS | 50 |
| LastuserID | int |  | 4 |
| Lastupdate | datetime |  | 8 |
| Version | varchar(10) | Latin1_General_CI_AS | 10 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

