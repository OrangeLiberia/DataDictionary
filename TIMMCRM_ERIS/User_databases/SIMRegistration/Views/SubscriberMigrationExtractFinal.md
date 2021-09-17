#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.SubscriberMigrationExtractFinal

# ![Views](../../../../Images/View32.png) [dbo].[SubscriberMigrationExtractFinal]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Created | 5:55:29 PM Sunday, February 12, 2017 |
| Last Modified | 1:55:39 PM Saturday, May 13, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | int | 4 | 0 - 0 |
| NamePrefix | varchar(3) | 3 |  |
| FirstName | varchar(255) | 255 |  |
| LastName | varchar(255) | 255 |  |
| MSISDN | varchar(10) | 10 |  |
| IdentificationNumber | varchar(10) | 10 |  |
| FormNumber | varchar(1) | 1 |  |
| DateOfBirth | varchar(30) | 30 |  |
| Gender | varchar(255) | 255 |  |
| Address | varchar(255) | 255 |  |
| District | varchar(255) | 255 |  |
| City | varchar(255) | 255 |  |
| State | varchar(255) | 255 |  |
| Country | varchar(1) | 1 |  |
| Description | varchar(1) | 1 |  |
| PreferredLanguage | varchar(7) | 7 |  |
| TypeOfIdentityProof | varchar(1) | 1 |  |
| TypeOfAddressProof | varchar(1) | 1 |  |
| TypeOfPhotoProof | varchar(1) | 1 |  |
| MobileGroupRoleID | varchar(9) | 9 |  |
| GradeCode | varchar(7) | 7 |  |
| TCPProfileID | varchar(20) | 20 |  |
| PrimaryAccount | varchar(1) | 1 |  |
| CustomerID | varchar(1) | 1 |  |
| AccountNumber | varchar(1) | 1 |  |
| AccountType | varchar(1) | 1 |  |
| WalletType | varchar(1) | 1 |  |
| UserStatus | varchar(1) | 1 |  |
| MiddleName | varchar(255) | 255 |  |
| Nationality | varchar(50) | 50 |  |
| IDType | varchar(1) | 1 |  |
| IDNumber | varchar(1) | 1 |  |
| PlaceOfIDIssued | varchar(1) | 1 |  |
| IssuedCountryCode | varchar(1) | 1 |  |
| ResidencyCountryCode | varchar(1) | 1 |  |
| IssuedDate | varchar(1) | 1 |  |
| IsIDExpires | varchar(1) | 1 |  |
| ExpireDate | varchar(1) | 1 |  |
| PostalCode | varchar(1) | 1 |  |
| EmployerName | varchar(1) | 1 |  |
| SubsID | int | 4 |  |
| USDBalance | decimal(12,2) | 9 |  |
| LRDBalance | decimal(12,2) | 9 |  |
| NewFirstName | varchar(50) | 50 |  |
| NewMiddleName | varchar(50) | 50 |  |
| NewLastName | varchar(50) | 50 |  |
| NewAddress | varchar(50) | 50 |  |
| NewNationality | varchar(50) | 50 |  |
| PIN | varchar(4) | 4 |  |
| GroupID | int | 4 |  |
| TCPProfileID_USD | varchar(20) | 20 |  |
| TCPProfileID_LRD | varchar(20) | 20 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE 
view [dbo].[SubscriberMigrationExtractFinal] as select * from SubscriberMigrationExtract7
GO

```


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

