#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.Retailers

# ![Views](../../../../Images/View32.png) [dbo].[Retailers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Created | 5:11:16 PM Saturday, March 18, 2017 |
| Last Modified | 5:11:16 PM Saturday, March 18, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | int | 4 | 0 - 0 |
| MSISDN | varchar(20) | 20 |  |
| USD | float | 8 |  |
| LRD | float | 8 |  |
| Other | float | 8 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
create view [dbo].[Retailers] as select * from Retailers5
GO

```


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

