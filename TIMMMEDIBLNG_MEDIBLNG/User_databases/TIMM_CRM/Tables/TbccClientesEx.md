#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TbccClientesEx

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccClientesEx]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccClientesEx: ClienteID](../../../../Images/pkcluster.png)](#indexes) | ClienteID | numeric(18,0) | 9 | NOT NULL |
|  | FirstName | nvarchar(200) | 400 | NULL allowed |
|  | MiddleName | nvarchar(200) | 400 | NULL allowed |
|  | LastName | nvarchar(200) | 400 | NULL allowed |
|  | DateBirth | smalldatetime | 4 | NULL allowed |
|  | MothersMaidenName | nvarchar(200) | 400 | NULL allowed |
|  | HomeAddress | nvarchar(200) | 400 | NULL allowed |
|  | Nationality | int | 4 | NULL allowed |
|  | Beneficiary | nvarchar(200) | 400 | NULL allowed |
|  | Email1 | nvarchar(200) | 400 | NULL allowed |
|  | Email2 | nvarchar(200) | 400 | NULL allowed |
|  | Email3 | nvarchar(200) | 400 | NULL allowed |
|  | PhoneNumber | nvarchar(max) | max | NULL allowed |
|  | Status | int | 4 | NULL allowed |
|  | IncomeAmountExpectancy | numeric(18,0) | 9 | NULL allowed |
|  | Equipment | bigint | 8 | NULL allowed |
|  | InternetFixed | bit | 1 | NULL allowed |
|  | InternetMobile | bit | 1 | NULL allowed |
|  | CompanyName | nvarchar(200) | 400 | NULL allowed |
|  | PositionInCompany | nvarchar(200) | 400 | NULL allowed |
|  | NumberOfEmployeesInCompany | smallint | 2 | NULL allowed |
|  | OfficeAddress | nvarchar(200) | 400 | NULL allowed |
|  | BankName | nvarchar(200) | 400 | NULL allowed |
|  | BankBranchName | nvarchar(200) | 400 | NULL allowed |
|  | BankAddress | nvarchar(200) | 400 | NULL allowed |
|  | BankAccountNumber | nvarchar(200) | 400 | NULL allowed |
|  | BankSwiftNumber | nvarchar(200) | 400 | NULL allowed |
|  | BankIBAN | nvarchar(200) | 400 | NULL allowed |
|  | BankIBA | nvarchar(200) | 400 | NULL allowed |
|  | TransactionSoldDate | smalldatetime | 4 | NULL allowed |
|  | TransactionPurchaseDate | smalldatetime | 4 | NULL allowed |
|  | TransactionValue | numeric(18,2) | 9 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | smalldatetime | 4 | NOT NULL |
|  | Remarks | varchar(8000) | 8000 | NULL allowed |
|  | SalesAgent | int | 4 | NULL allowed |
|  | PaymentTerm | tinyint | 1 | NULL allowed |
|  | NextContact | datetime | 8 | NULL allowed |
|  | NextContactFrom | varchar(5) | 5 | NULL allowed |
|  | NextContactTo | varchar(5) | 5 | NULL allowed |
|  | Conversion | bit | 1 | NULL allowed |
|  | IncorporationNumber | nvarchar(20) | 40 | NULL allowed |
|  | NoBankAccount | bit | 1 | NULL allowed |
|  | AnonymClient | bit | 1 | NULL allowed |
|  | FinanceAgent | int | 4 | NULL allowed |
|  | TelemarketingAgent | int | 4 | NULL allowed |
|  | EquipmentOffer | bigint | 8 | NULL allowed |
|  | Mainkey | varchar(20) | 20 | NOT NULL |
|  | Converted | bit | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

