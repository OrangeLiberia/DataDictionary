#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.SIMRegistrations_HIST

# ![Tables](../../../../Images/Table32.png) [dbo].[SIMRegistrations_HIST]

---

## <a name="#description"></a>MS_Description

SIM Registration Information History

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrations_HIST: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | _ID_ |
|  | MSISDN | varchar(20) | 20 | NOT NULL | _Subscriber MSISDN_ |
|  | APP | varchar(10) | 10 | NOT NULL | _App Identification (MIG - Migration, SIMREG - Simregistration App, TIMM-CC - CRM)_ |
|  | ExecState | smallint | 2 | NOT NULL | _Registration execution state_ |
|  | ReturnID | smallint | 2 | NULL allowed | _Registration returned value_ |
|  | SubsID | numeric(18,0) | 9 | NULL allowed | _CRM ServiceID_ |
|  | TIMMAccaoID | numeric(18,0) | 9 | NULL allowed | _CRM Action id_ |
|  | TIMMTipoAccao | varchar(50) | 50 | NULL allowed | _CRM Action type_ |
|  | NTIMMPics | int | 4 | NULL allowed | _Quantity of images scanned_ |
|  | FullName | varchar(150) | 150 | NULL allowed | _Subscriber full name_ |
|  | FirstName | varchar(50) | 50 | NULL allowed | _Subscriber name_ |
|  | MiddleName | varchar(50) | 50 | NULL allowed | _Subscriber middle name_ |
|  | LastName | varchar(50) | 50 | NULL allowed | _Subscriber last name_ |
|  | BirthDate | datetime | 8 | NULL allowed | _Subscriber birth date_ |
|  | BirthPlace | varchar(50) | 50 | NULL allowed | _Subscriber birth place_ |
|  | Gender | varchar(20) | 20 | NULL allowed | _Subscriber gender (Male,Female, Not Applicable)_ |
|  | MaritalStatus | varchar(20) | 20 | NULL allowed | _Subscriber marital status (Single, Married, Divorced, Widow, Other, Not Applicable)_ |
|  | IDCard | varchar(20) | 20 | NULL allowed | _Identification Card Number_ |
|  | IDCardType | varchar(20) | 20 | NULL allowed | _Identification Card Type (Birth Certificate, Driver License, Driver's Licence, Employee Card, Military card, National ID Card, Other, Passport, Social Secutiry card, Student card, Voter ID card, Voter's ID, Invalid National ID)_ |
|  | IDFrontPicture | bigint | 8 | NULL allowed | _ID for Subscriber photo image [see SIMMRegistrationPictures](SIMMRegistrationPictures)_ |
|  | IDCardPicture | bigint | 8 | NULL allowed | _ID for Subscriber registration card scan [see SIMMRegistrationPictures](SIMMRegistrationPictures)_ |
|  | IDContractPicture | bigint | 8 | NULL allowed | _ID for Subscriber registration contract scan [see SIMMRegistrationPictures](SIMMRegistrationPictures)_ |
|  | AddressType | varchar(20) | 20 | NULL allowed | _Type of address (Business, Other, Residence, School, Work)_ |
|  | AddressCounty | varchar(30) | 30 | NULL allowed | _Subscriber's address country_ |
|  | Address | varchar(150) | 150 | NULL allowed | _Subscriber's address_ |
|  | EMail | varchar(100) | 100 | NULL allowed | _Subscriber's eMail_ |
|  | Job | varchar(50) | 50 | NULL allowed | _Subscriber's Job_ |
|  | Country | varchar(50) | 50 | NULL allowed | _Subscriber's country_ |
|  | ConfirmationCode | varchar(10) | 10 | NULL allowed |  |
|  | RegistrationDate | datetime | 8 | NULL allowed | _Datetime of registration_ |
|  | EntryDate | datetime | 8 | NOT NULL | _Datetime of registration entry date_ |
|  | DownloadDate | datetime | 8 | NULL allowed |  |
|  | ExecutionDate | datetime | 8 | NULL allowed | _Datetime of registration execution_ |
|  | AgentID | int | 4 | NULL allowed | _AgentID [see AgentsWhitelist](AgentsWhitelist) or CRM User ID [see Account](../../../../LOCAL/TIMM_Admin/User_databases/Tables/AdminAccount)_ |
|  | AgentUserName | varchar(20) | 20 | NULL allowed | _Agent username_ |
|  | AppVersion | varchar(10) | 10 | NULL allowed | _SIMRegistration App version used for registration_ |
|  | AgentMSISDN | varchar(20) | 20 | NULL allowed | _Agent MSISDN_ |
|  | AgentIMEI | varchar(20) | 20 | NULL allowed | _Agent Device Identification_ |
|  | AgentICCID | varchar(20) | 20 | NULL allowed | _Agent SIM identification_ |
|  | GPSLocation | varchar(50) | 50 | NULL allowed | _GPS location_ |
|  | CellID | int | 4 | NULL allowed | _Not used_ |
|  | MobileMoney | bit | 1 | NULL allowed | _Indicates if it's a mobile money registration (0 - No, 1 - Yes)_ |
|  | NextOfKinName | varchar(150) | 150 | NULL allowed |  |
|  | NextOfKinPhoneNumber | varchar(20) | 20 | NULL allowed |  |
|  | NextOfKinEmail | varchar(100) | 100 | NULL allowed |  |
|  | MobileMoneyApp | varchar(10) | 10 | NULL allowed | _Orange Money Platform used ( OM - Tango )_ |
|  | MobileMoneyID | varchar(100) | 100 | NULL allowed | _Orange Money success registration message_ |
|  | MobileMoneyMsg | varchar(max) | max | NULL allowed | _Orange Money failure registration message_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrations_HIST: ID](../../../../Images/pkcluster.png)](#indexes) | PK_SIMRegistrations_HIST | ID | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

