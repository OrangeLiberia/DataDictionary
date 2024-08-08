#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.tmp_AgreementInsertTrace

# ![Tables](../../../../Images/Table32.png) [dbo].[tmp_AgreementInsertTrace]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|
| id | int | 4 | NOT NULL | 1 - 1 |  |
| dt | datetime | 8 | NOT NULL |  | (getdate()) |
| agreement | xml | max | NULL allowed |  |  |
| zones | xml | max | NULL allowed |  |  |
| schedules | xml | max | NULL allowed |  |  |
| rates | xml | max | NULL allowed |  |  |
| services | xml | max | NULL allowed |  |  |
| zoneCountries | xml | max | NULL allowed |  |  |
| LastUserID | int | 4 | NULL allowed |  |  |
| oldIdAgreement | bigint | 8 | NULL allowed |  |  |
| FutureAgreement | bit | 1 | NULL allowed |  |  |
| Ranges | xml | max | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

