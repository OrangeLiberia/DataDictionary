#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.vws_SIMRegistrationAll

# ![Views](../../../../Images/View32.png) [dbo].[vws_SIMRegistrationAll]

---

## <a name="#description"></a>MS_Description

View all the registrations History + Current

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Schema Bound | YES |
| Created | 12:24:09 PM Wednesday, May 4, 2016 |
| Last Modified | 11:48:24 AM Friday, December 18, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Type | varchar(6) | 6 |
| ID | bigint | 8 |
| MSISDN | varchar(20) | 20 |
| APP | varchar(10) | 10 |
| ExecState | smallint | 2 |
| ReturnID | smallint | 2 |
| SubsID | numeric(18,0) | 9 |
| TIMMAccaoID | numeric(18,0) | 9 |
| TIMMTipoAccao | varchar(50) | 50 |
| FullName | varchar(150) | 150 |
| FirstName | varchar(50) | 50 |
| MiddleName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| BirthDate | datetime | 8 |
| BirthPlace | varchar(50) | 50 |
| Gender | varchar(20) | 20 |
| MaritalStatus | varchar(20) | 20 |
| IDCard | varchar(20) | 20 |
| IDCardType | varchar(20) | 20 |
| IDFrontPicture | bigint | 8 |
| IDCardPicture | bigint | 8 |
| IDContractPicture | bigint | 8 |
| AddressType | varchar(20) | 20 |
| AddressCounty | varchar(30) | 30 |
| Address | varchar(150) | 150 |
| EMail | varchar(100) | 100 |
| Job | varchar(50) | 50 |
| Country | varchar(50) | 50 |
| ConfirmationCode | varchar(10) | 10 |
| AgentUserName | varchar(20) | 20 |
| AgentID | int | 4 |
| EntryDate | datetime | 8 |
| RegistrationDate | datetime | 8 |
| DownloadDate | datetime | 8 |
| MobileMoney | bit | 1 |
| AppVersion | varchar(10) | 10 |
| NextOfKinName | varchar(150) | 150 |
| NextOfKinPhoneNumber | varchar(20) | 20 |
| NextOfKinEmail | varchar(100) | 100 |
| AgentMSISDN | varchar(20) | 20 |
| AgentIMEI | varchar(20) | 20 |
| AgentICCID | varchar(20) | 20 |
| GPSLocation | varchar(50) | 50 |
| CellID | int | 4 |
| NTIMMPics | int | 4 |
| MobileMoneyApp | varchar(10) | 10 |
| MobileMoneyID | varchar(100) | 100 |
| MobileMoneyMsg | varchar(max) | max |


---

## <a name="#sqlscript"></a>SQL Script

```sql



CREATE view [dbo].[vws_SIMRegistrationAll]
with schemabinding
as
	SELECT	'Buffer' as Type, [ID],[MSISDN],[APP],[ExecState],[ReturnID],[SubsID],[TIMMAccaoID],[TIMMTipoAccao],
			[FullName],[FirstName],[MiddleName],[LastName],[BirthDate],[BirthPlace],[Gender],[MaritalStatus],
			[IDCard],[IDCardType],[IDFrontPicture],[IDCardPicture],IDContractPicture, [AddressType],[AddressCounty],[Address],-- IDSignaturePicture,
			[EMail],[Job],[Country],[ConfirmationCode],[AgentUserName],[AgentID],[EntryDate],[RegistrationDate],[DownloadDate],
			MobileMoney, AppVersion, NextOfKinName, NextOfKinPhoneNumber, NextOfKinEmail, AgentMSISDN, AgentIMEI, AgentICCID, GPSLocation, CellID, NTIMMPics, MobileMoneyApp, [MobileMoneyID], MobileMoneyMsg
	FROM	[dbo].[SIMRegistrationBuffer]
	UNION ALL
	SELECT	'Hist' as Type, [ID],[MSISDN],[APP],[ExecState],[ReturnID],[SubsID],[TIMMAccaoID],[TIMMTipoAccao],
			[FullName],[FirstName],[MiddleName],[LastName],[BirthDate],[BirthPlace],[Gender],[MaritalStatus],
			[IDCard],[IDCardType],[IDFrontPicture],[IDCardPicture],IDContractPicture, [AddressType],[AddressCounty],[Address], --IDSignaturePicture,
			[EMail],[Job],[Country],[ConfirmationCode],[AgentUserName],[AgentID],[EntryDate],[RegistrationDate],[DownloadDate],
			MobileMoney, AppVersion, NextOfKinName, NextOfKinPhoneNumber, NextOfKinEmail, AgentMSISDN, AgentIMEI, AgentICCID, GPSLocation, CellID, NTIMMPics, MobileMoneyApp, [MobileMoneyID], MobileMoneyMsg
	FROM	[dbo].[SIMRegistrations]
GO
EXEC sp_addextendedproperty N'MS_Description', N'View all the registrations History + Current', 'SCHEMA', N'dbo', 'VIEW', N'vws_SIMRegistrationAll', NULL, NULL
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[SIMRegistrationBuffer]](../Tables/SIMRegistrationBuffer.md)
* [[dbo].[SIMRegistrations]](../Tables/SIMRegistrations.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[sps_SIMRegistrationClose]](../Programmability/Stored_Procedures/sps_SIMRegistrationClose.md)
* [[dbo].[sps_SIMRegistrationUploadTIMMPics]](../Programmability/Stored_Procedures/sps_SIMRegistrationUploadTIMMPics.md)


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

