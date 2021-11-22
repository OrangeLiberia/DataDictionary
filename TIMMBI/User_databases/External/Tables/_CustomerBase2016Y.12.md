#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._CustomerBase2016Y.12

# ![Tables](../../../../Images/Table32.png) [dbo].[_CustomerBase2016Y.12]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ServicoID | numeric(18,0) | 9 | NOT NULL |
| MSISDN | varchar(51) | 51 | NOT NULL |
| SimType | varchar(4) | 4 | NOT NULL |
| DataService | varchar(6) | 6 | NOT NULL |
| BIFirstActivity | datetime | 8 | NULL allowed |
| BILastActivity | datetime | 8 | NULL allowed |
| BIActivityBeforeTF | bit | 1 | NULL allowed |
| BIActivityDuringTF | bit | 1 | NULL allowed |
| DataMB | numeric(38,6) | 17 | NOT NULL |
| DataRevenue | decimal(38,5) | 17 | NOT NULL |
| DataServiceY | tinyint | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

