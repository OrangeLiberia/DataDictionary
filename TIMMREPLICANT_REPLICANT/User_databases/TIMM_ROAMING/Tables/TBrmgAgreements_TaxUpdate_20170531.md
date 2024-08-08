#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgAgreements_TaxUpdate_20170531

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgAgreements_TaxUpdate_20170531]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| IDAgreement | bigint | 8 | NOT NULL | 1 - 1 |
| AgreementName | varchar(200) | 200 | NULL allowed |  |
| Version | varchar(10) | 10 | NULL allowed |  |
| IDHomeOperator | int | 4 | NOT NULL |  |
| AgreementType | varchar(10) | 10 | NULL allowed |  |
| IDOperator | int | 4 | NOT NULL |  |
| IDParentOperator | int | 4 | NULL allowed |  |
| PLMNIDParentOperator | varchar(5) | 5 | NULL allowed |  |
| AgreementStatusID | int | 4 | NULL allowed |  |
| DateBegin | datetime | 8 | NULL allowed |  |
| DateEnd | datetime | 8 | NULL allowed |  |
| TaxesApplied | int | 4 | NULL allowed |  |
| TipoMoedaID | int | 4 | NULL allowed |  |
| LastuserID | int | 4 | NOT NULL |  |
| Lastupdate | datetime | 8 | NOT NULL |  |
| RatingType | varchar(20) | 20 | NOT NULL |  |
| PLMNIDHomeOperator | varchar(7) | 7 | NULL allowed |  |
| PLMNIDOperator | varchar(7) | 7 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

