#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._PrePayNationTDR

# ![Tables](../../../../Images/Table32.png) [dbo].[_PrePayNationTDR]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| SubsID | int | 4 | NOT NULL |
| MSISDN | varchar(20) | 20 | NULL allowed |
| ChargeableAmount | numeric(24,6) | 13 | NOT NULL |
| TDRTime | datetime | 8 | NOT NULL |
| TDREndingBalance | numeric(24,6) | 13 | NOT NULL |
| WalletID | int | 4 | NOT NULL |
| CardSerialNumber | nvarchar(4000) | 8000 | NULL allowed |
| DT | varchar(10) | 10 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

