#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.vws_SIMRegistrationPictures

# ![Views](../../../../Images/View32.png) [dbo].[vws_SIMRegistrationPictures]

---

## <a name="#description"></a>MS_Description

View all the registrations Pictures

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Created | 12:25:10 PM Wednesday, May 4, 2016 |
| Last Modified | 12:25:10 PM Wednesday, May 4, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | bigint | 8 | 0 - 0 |
| PictureFile | varchar(100) | 100 |  |
| Type | varchar(10) | 10 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

create view [dbo].[vws_SIMRegistrationPictures] as
	select ID, PictureFile,	[Type] from [SIMRegistrationPictures] 
GO
EXEC sp_addextendedproperty N'MS_Description', N'View all the registrations Pictures', 'SCHEMA', N'dbo', 'VIEW', N'vws_SIMRegistrationPictures', NULL, NULL
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[SIMRegistrationPictures]](../Tables/SIMRegistrationPictures.md)


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

