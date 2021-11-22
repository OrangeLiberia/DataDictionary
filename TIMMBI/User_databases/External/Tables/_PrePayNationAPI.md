#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._PrePayNationAPI

# ![Tables](../../../../Images/Table32.png) [dbo].[_PrePayNationAPI]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ID | bigint | 8 | NOT NULL |
| Client | varchar(50) | 50 | NULL allowed |
| MSISDN | varchar(20) | 20 | NULL allowed |
| Parameters | varchar(max) | max | NULL allowed |
| Amount | float | 8 | NULL allowed |
| AmountParam | float | 8 | NULL allowed |
| Fee | float | 8 | NULL allowed |
| ExternalID | varchar(50) | 50 | NULL allowed |
| ReturnValue | bit | 1 | NOT NULL |
| ResultID | bigint | 8 | NOT NULL |
| Reply | varchar(max) | max | NULL allowed |
| DateTime | datetime | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

