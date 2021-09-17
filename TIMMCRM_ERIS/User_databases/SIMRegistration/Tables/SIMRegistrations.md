#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.SIMRegistrations

# ![Tables](../../../../Images/Table32.png) [dbo].[SIMRegistrations]

---

## <a name="#description"></a>MS_Description

SIM Registration Information

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrations: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL |  | _ID_ |
| [![Indexes IX_SIMREG_QUEUE, IX_SIMRegistrations_MSISDN, IX_SIMRegistrations_TIMM](../../../../Images/Index.png)](#indexes)(3) | MSISDN | varchar(20) | 20 | NOT NULL |  | _Subscriber MSISDN_ |
| [![Indexes IX_GRAFANA](../../../../Images/Index.png)](#indexes) | APP | varchar(10) | 10 | NOT NULL |  | _App Identification (MIG - Migration, SIMREG - Simregistration App, TIMM-CC - CRM)_ |
| [![Indexes IX_SIMREG_QUEUE,IX_RegistrationStats](../../../../Images/Index.png)](#indexes)(2) | ExecState | smallint | 2 | NOT NULL |  | _Registration execution state_ |
| [![Indexes IX_GRAFANA,IX_SIMREG_QUEUE,IX_RegistrationStats](../../../../Images/Index.png)](#indexes)(3) | ReturnID | smallint | 2 | NULL allowed |  | _Registration returned value_ |
|  | SubsID | numeric(18,0) | 9 | NULL allowed |  | _CRM ServiceID_ |
| [![Indexes IX_SIMRegistrations_TIMM](../../../../Images/Index.png)](#indexes) | TIMMAccaoID | numeric(18,0) | 9 | NULL allowed |  | _CRM Action id_ |
| [![Indexes IX_SIMRegistrations_TIMM](../../../../Images/Index.png)](#indexes) | TIMMTipoAccao | varchar(50) | 50 | NULL allowed |  | _CRM Action type_ |
|  | NTIMMPics | int | 4 | NULL allowed |  | _Quantity of images scanned_ |
|  | FullName | varchar(150) | 150 | NULL allowed |  | _Subscriber full name_ |
|  | FirstName | varchar(50) | 50 | NULL allowed |  | _Subscriber name_ |
|  | MiddleName | varchar(50) | 50 | NULL allowed |  | _Subscriber middle name _ |
|  | LastName | varchar(50) | 50 | NULL allowed |  | _Subscriber last name_ |
|  | BirthDate | datetime | 8 | NULL allowed |  | _Subscriber birth date_ |
|  | BirthPlace | varchar(50) | 50 | NULL allowed |  | _Subscriber birth place_ |
|  | Gender | varchar(20) | 20 | NULL allowed |  | _Subscriber gender (Male,Female, Not Applicable)_ |
|  | MaritalStatus | varchar(20) | 20 | NULL allowed |  | _Subscriber marital status (Single, Married, Divorced, Widow, Other, Not Applicable)_ |
|  | IDCard | varchar(20) | 20 | NULL allowed |  | _Identification Card Number_ |
|  | IDCardType | varchar(20) | 20 | NULL allowed |  | _Identification Card Type (Birth Certificate, Driver License, Driver's Licence, Employee Card, Military card, National ID Card, Other, Passport, Social Secutiry card, Student card, Voter ID card, Voter's ID, Invalid National ID)_ |
|  | IDFrontPicture | bigint | 8 | NULL allowed |  | _ID for Subscriber photo image [see SIMRegistrationPictures](SIMRegistrationPictures.md)_ |
|  | IDCardPicture | bigint | 8 | NULL allowed |  | _ID for Subscriber registration card scan [see SIMRegistrationPictures](SIMRegistrationPictures.md)_ |
|  | IDContractPicture | bigint | 8 | NULL allowed |  | _ID for Subscriber registration contract scan [see SIMRegistrationPictures](SIMRegistrationPictures.md)_ |
|  | AddressType | varchar(20) | 20 | NULL allowed |  | _Type of address (Business, Other, Residence, School, Work)_ |
|  | AddressCounty | varchar(30) | 30 | NULL allowed |  | _Subscriber's address country_ |
|  | Address | varchar(150) | 150 | NULL allowed |  | _Subscriber's address_ |
|  | EMail | varchar(100) | 100 | NULL allowed |  | _Subscriber's eMail_ |
|  | Job | varchar(50) | 50 | NULL allowed |  | _Subscriber's Job_ |
|  | Country | varchar(50) | 50 | NULL allowed |  | _Subscriber's country_ |
|  | ConfirmationCode | varchar(10) | 10 | NULL allowed |  |  |
|  | RegistrationDate | datetime | 8 | NULL allowed |  | _Datetime of registration_ |
| [![Indexes IX_GRAFANA,IX_RegistrationStats,IX_SIMRegistrations_MSISDN](../../../../Images/Index.png)](#indexes)(3) | EntryDate | datetime | 8 | NOT NULL |  | _Datetime of registration entry date_ |
|  | DownloadDate | datetime | 8 | NULL allowed |  |  |
|  | ExecutionDate | datetime | 8 | NULL allowed | (getdate()) | _Datetime of registration execution_ |
| [![Indexes IX_GRAFANA,IX_RegistrationStats](../../../../Images/Index.png)](#indexes)(2) | AgentID | int | 4 | NULL allowed |  | _AgentID [see AgentsWhitelist](AgentsWhitelist.md) or CRM User ID [see Account](../../../../LOCAL/TIMM_Admin/User_databases/Tables/AdminAccount.md)_ |
|  | AgentUserName | varchar(20) | 20 | NULL allowed |  | _Agent username_ |
|  | AppVersion | varchar(10) | 10 | NULL allowed |  | _SIMRegistration App version used for registration_ |
|  | AgentMSISDN | varchar(20) | 20 | NULL allowed |  | _Agent MSISDN_ |
|  | AgentIMEI | varchar(20) | 20 | NULL allowed |  | _Agent Device Identification_ |
|  | AgentICCID | varchar(20) | 20 | NULL allowed |  | _Agent SIM identification _ |
|  | GPSLocation | varchar(50) | 50 | NULL allowed |  | _GPS location_ |
|  | CellID | int | 4 | NULL allowed |  | _Not used_ |
| [![Indexes IX_RegistrationStats](../../../../Images/Index.png)](#indexes) | MobileMoney | bit | 1 | NULL allowed |  | _Indicates if it's a mobile money registration (0 - No, 1 - Yes)_ |
|  | NextOfKinName | varchar(150) | 150 | NULL allowed |  | _Name of next of kin_ |
|  | NextOfKinPhoneNumber | varchar(20) | 20 | NULL allowed |  | _Phone number of next of kin_ |
|  | NextOfKinEmail | varchar(100) | 100 | NULL allowed |  | _EMail number of next of kin_ |
|  | MobileMoneyApp | varchar(10) | 10 | NULL allowed |  | _Orange Money Platform used ( OM - Tango )_ |
|  | MobileMoneyID | varchar(100) | 100 | NULL allowed |  | _Mobile Money success registration message_ |
|  | MobileMoneyMsg | varchar(max) | max | NULL allowed |  | _Mobile Money failure registration message_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrations: ID](../../../../Images/pkcluster.png)](#indexes) | PK_SIMRegistrations | ID |  | YES |
|  | IX_GRAFANA | EntryDate | APP, ReturnID, AgentID |  |
|  | IX_RegistrationStats | ExecState, ReturnID, AgentID | EntryDate, MobileMoney |  |
|  | IX_SIMREG_QUEUE | ExecState, ReturnID | MSISDN |  |
|  | IX_SIMRegistrations_MSISDN | MSISDN, EntryDate |  |  |
|  | IX_SIMRegistrations_TIMM | TIMMAccaoID, MSISDN, TIMMTipoAccao |  |  |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

