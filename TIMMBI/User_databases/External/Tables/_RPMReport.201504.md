#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._RPMReport.201504

# ![Tables](../../../../Images/Table32.png) [dbo].[_RPMReport.201504]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| IDDimDate | int | 4 | NOT NULL |
| DT | smalldatetime | 4 | NOT NULL |
| Year | smallint | 2 | NOT NULL |
| Month | varchar(7) | 7 | NOT NULL |
| IDTopGroup | int | 4 | NULL allowed |
| GroupName | varchar(20) | 20 | NULL allowed |
| IDDest | int | 4 | NULL allowed |
| Name | varchar(53) | 53 | NULL allowed |
| NameDest | varchar(20) | 20 | NULL allowed |
| RealDurMin | numeric(26,6) | 13 | NULL allowed |
| BillDurMin | numeric(26,6) | 13 | NULL allowed |
| Consumed | float | 8 | NULL allowed |
| Fees | float | 8 | NULL allowed |
| Amount | float | 8 | NULL allowed |
| Source | varchar(5) | 5 | NULL allowed |
| NSubs | int | 4 | NULL allowed |
| NSubsGroup | int | 4 | NULL allowed |
| NSubsTotal | int | 4 | NULL allowed |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

