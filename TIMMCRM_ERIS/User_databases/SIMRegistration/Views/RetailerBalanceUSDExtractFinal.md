#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.RetailerBalanceUSDExtractFinal

# ![Views](../../../../Images/View32.png) [dbo].[RetailerBalanceUSDExtractFinal]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Created | 5:45:16 PM Friday, May 12, 2017 |
| Last Modified | 1:55:53 PM Saturday, May 13, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | int | 4 | 0 - 0 |
| MobileNumber | varchar(10) | 10 |  |
| Amount | decimal(12,2) | 9 |  |
| FirstName | varchar(255) | 255 |  |
| LastName | varchar(255) | 255 |  |
| IdNumber | varchar(10) | 10 |  |
| Remarks | varchar(2) | 2 |  |
| UserType | varchar(10) | 10 |  |
| GroupID | int | 4 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE 
view [dbo].[RetailerBalanceUSDExtractFinal] as select * from RetailerBalanceUSDExtract7
GO

```


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

