#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.RetailerPINExtractFinal

# ![Views](../../../../Images/View32.png) [dbo].[RetailerPINExtractFinal]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Created | 11:40:06 AM Saturday, May 13, 2017 |
| Last Modified | 1:55:59 PM Saturday, May 13, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| MSISDN | varchar(20) | 20 |
| UserType | varchar(20) | 20 |
| OLDPIN | varchar(4) | 4 |
| NEWPIN | varchar(4) | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE 
view [dbo].[RetailerPINExtractFinal] as select * from RetailersPINMigrationExtract7
GO

```


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

