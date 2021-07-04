#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._CustomerBase2016Q3.09

# ![Tables](../../../../Images/Table32.png) [dbo].[_CustomerBase2016Q3.09]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| MSISDN | varchar(51) | 51 | NOT NULL |
| SimType | varchar(4) | 4 | NOT NULL |
| DataService | varchar(6) | 6 | NOT NULL |
| BIFirstActivity | datetime | 8 | NULL allowed |
| BILastActivity | datetime | 8 | NULL allowed |
| BIActivityBeforeTF | bit | 1 | NULL allowed |
| BIActivityDuringTF | bit | 1 | NULL allowed |
| DataMB | numeric(38,6) | 17 | NOT NULL |
| DataRevenue | decimal(38,5) | 17 | NOT NULL |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

