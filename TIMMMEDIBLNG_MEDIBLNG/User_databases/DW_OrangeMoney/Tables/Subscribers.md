#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.Subscribers

# ![Tables](../../../../Images/Table32.png) [dbo].[Subscribers]

---

## <a name="#description"></a>MS_Description

New Subscribers and Subscribers updates

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Subscribers_V11: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL | _Unique File Identifier_ |
| [![Cluster Primary Key PK_Subscribers_V11: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | _Unique Data Line within a file_ |
| [![Cluster Primary Key PK_Subscribers_V11: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Date of the file_ |
|  | CurrencyType | varchar(16) | 16 | NOT NULL | _Currency (USD/LRD)_ |
|  | USERID | varchar(20) | 20 | NOT NULL |  |
|  | PROFILE_ID | varchar(20) | 20 | NULL allowed | _Id of the Profile assigned to the PRIMARY WALLET of the subscriber. A profile is a set of thresholds applied to the Orange Money user (maximum amounts and numbers of transactions per day, week, month, etc.)_ |
|  | PARENT_USER_ID | varchar(20) | 20 | NULL allowed | _User_id of the subscribers parent user_ |
|  | PARENT_USER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN if the subscribers parent user_ |
|  | MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the subscriber (Subscriber mobile number)_ |
|  | USER_NAME_PREFIX | varchar(100) | 100 | NULL allowed | _Prefix to apply to the subscriber name _ |
|  | USER_FIRST_NAME | varchar(80) | 80 | NULL allowed | _First name of the Subscriber_ |
|  | USER_LAST_NAME | varchar(80) | 80 | NULL allowed | _Last name of the subscriber_ |
|  | USER_SHORT_NAME | varchar(16) | 16 | NULL allowed | _Middle name of the subscriber_ |
|  | DOB | varchar(32) | 32 | NULL allowed | _Date of birth of the subscriber_ |
|  | REGISTERED_ON | datetime | 8 | NULL allowed | _Date of the subscribers registration_ |
|  | ADDRESS1 | varchar(50) | 50 | NULL allowed | _Address of the subscriber_ |
|  | ADDRESS2 | varchar(50) | 50 | NULL allowed | _District of the subscriber_ |
|  | STATE | varchar(30) | 30 | NULL allowed | _Value of the state field of the subscriber. This field can be used to recognize special subscribers (transactions of these specific subscribers can then be count separately, cf. specifications of transaction TAGS)_ |
|  | CITY | varchar(30) | 30 | NULL allowed | _City of the subscriber_ |
|  | COUNTRY | varchar(20) | 20 | NULL allowed | _Country of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | SSN | varchar(15) | 15 | NULL allowed | _Value of the SSN field of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | DESIGNATION | varchar(30) | 30 | NULL allowed | _Value of the Designation field of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | DIVISION | varchar(30) | 30 | NULL allowed | _Value of the Division field of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | CONTACT_PERSON | varchar(80) | 80 | NULL allowed | _Value of the Contact_person field of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | CONTACT_NO | varchar(50) | 50 | NULL allowed | _Value of the Contact_no field of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | EMPLOYEE_CODE | varchar(12) | 12 | NULL allowed | _Value of the Employee_code field of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | SEX | varchar(10) | 10 | NULL allowed | _Gender of the Subscriber. GEN_FEM, GEN_MAL, null_ |
|  | ID_NUMBER | varchar(40) | 40 | NULL allowed | _External code of the Subscriber (used to store the number of the users identity card)_ |
|  | E_MAIL | varchar(60) | 60 | NULL allowed | _E_mail address of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | WEB_LOGIN | varchar(20) | 20 | NULL allowed | _Login of the Subscriber. Always null for Subscribers as the field is not available in the Tango web interface_ |
|  | ACCOUNT_STATUS | varchar(2) | 2 | NULL allowed | _Status of the Subscriber : Y = Activated, S = Suspended, N = Deleted (Deteted means : deactivated with no possibility to reactivate)_ |
|  | CREATION_DATE | datetime | 8 | NULL allowed | _Date of the subscribers creation (same date than in field registered_on)_ |
|  | CREATED_BY | varchar(20) | 20 | NULL allowed | _User_id of the user that have registered the Subscriber.. Sometimes the user_id stored here does not really correspond to the channel user that have registered the Subscriber. For example, for Nomade/USSD subscriptions, the user_id here is the one of the Nomad user (and the user_id of the channel is indicated in the Remarks field). And when the registration is done through a call center, the user_id here is the one of the mirror-user of the channel user (and it is not possible to directly identify the real channel user linked to this mirror-account)._ |
|  | CREATED_BY_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the user that have registered the Subscriber_ |
|  | NOMADE_CREATED_BY | varchar(10) | 10 | NULL allowed | _Will be filled with the MSISDN of the channel user who has registered the subscriber in case of Nomad or USSD registration _ |
|  | LEVEL1_APPROVED_ON | datetime | 8 | NULL allowed | _Date of the first level of approval of the subscribers activation. Always null for Subscribers (as no approval is needed for subscribers activation), but present in this subscribers export in order to follow the same file format than the Channel Users export._ |
|  | LEVEL1_APPROVED_BY | varchar(30) | 30 | NULL allowed | _user_id of the Orange Money user who has validated the subscribers activation at the first level of approval. Always null for Subscribers (as no approval is needed for subscribers activation), but present in this subscribers export in order to follow the same file format than the Channel Users export._ |
|  | LEVEL2_APPROVED_ON | datetime | 8 | NULL allowed | _Date of the second/last level of approval of the subscribers activation_ |
|  | LEVEL2_APPROVED_BY | varchar(30) | 30 | NULL allowed | _user_id of the Orange Money user who has validated the subscribers activation at the second/last level of approval_ |
|  | OWNER_ID | varchar(20) | 20 | NULL allowed | _User_id of the subscribers owner_ |
|  | OWNER_MSISDN | varchar(15) | 15 | NULL allowed | _MSISDN of the subscribers owner_ |
|  | USER_DOMAIN_CODE | varchar(10) | 10 | NULL allowed | _Domain code of the Subscriber_ |
|  | USER_CATEGORY_CODE | varchar(10) | 10 | NULL allowed | _Category code of the Subscriber_ |
|  | USER_GRADE_NAME | varchar(40) | 40 | NULL allowed | _Name (and not code) of the Subscriber grade_ |
|  | MODIFIED_BY | varchar(30) | 30 | NULL allowed | _User_id of the user that have done the last subscribers data modification_ |
|  | MODIFIED_ON | datetime | 8 | NULL allowed | _Date of the last subscribers data modification_ |
|  | MODIFIED_APPROVED_BY | varchar(25) | 25 | NULL allowed | _Does not correspond to any Subscriber field, present only  to follow the same file format than the Channel Users export.. Always null for Subscribers_ |
|  | MODIFIED_APPROVED_ON | datetime | 8 | NULL allowed | _Does not correspond to any Subscriber field, present only  to follow the same file format than the Channel Users export.. Always null for Subscribers_ |
|  | DELETED_ON | datetime | 8 | NULL allowed | _Date of subscribers deletion_ |
|  | DEACTIVATION_BY | varchar(50) | 50 | NULL allowed | _User_id of the Channel user (or Operator user) that have deleted the Subscriber. Sometimes empty whereas the subscriber has been deactivated (status _ |
|  | DEPARTMENT | varchar(30) | 30 | NULL allowed | _Value of the Department field of teh Subscriber. Always null for Subscribers_ |
|  | REGISTRATION_FORM_NUMBER | varchar(20) | 20 | NULL allowed | _Form number used for the subscribers registration_ |
|  | REMARKS | varchar(100) | 100 | NULL allowed | _Value of the Description field of the Subscriber. Can contain any information manually entered in the Tango web interface_ |
|  | GEOGRAPHICAL_DOMAIN | varchar(50) | 50 | NULL allowed | _Geographical domain name of the Subscriber_ |
|  | GROUP_ROLE | varchar(35) | 35 | NULL allowed | _Does not correspond to any Subscriber field, present only  to follow the same file format than the Channel Users export.. Always null for Subscribers_ |
|  | FIRST_TRANSACTION_ON | datetime | 8 | NULL allowed | _Date of the first transaction TS for NEW Subscriber only (used to know if the user realizes a transaction on the same day than his registration). Only filled when Subscriber CREATION (and null when Subscriber modification/desactivation)_ |
|  | COMPANY_CODE | varchar(15) | 15 | NULL allowed | _Value of the user_code field of the Subscriber. Always null for Subscribers_ |
|  | USER_TYPE | varchar(10) | 10 | NULL allowed | _User type_ |
|  | ACTION_TYPE | varchar(20) | 20 | NULL allowed | _This field indicates wether the Subscriber is logged because of its creation, activation, desactivation or modification. Indeed, this field contains the value CREATION, ACTIVATION, DESACTIVATION or MODIFICATION according to the following rules:<br />- value CREATION when the logged Subscriber is a new one (registered on the day targetted by the data extraction)<br />- value ACTIVATION when the Subscriber registration has been validated on the day targetted by the data extraction (no such validation for Subscriber, this rule only applies to Channel Users).<br />- value DESACTIVATION when the Subscriber has been deleted on the day targetted by the data extraction<br />- value MODIFICATION when the Subscriber has already been logged when created (on a previous day), but has been modified on the day targetted by the data extraction.<br />- value CREATION_DESACT when the Subscriber has been created and then deleted on the day targetted by the data extraction<br />- value ACTIVATION_DESACT when the Subscriber registration has been validated and then the Subscriber deleted on the day targetted by the data extraction_ |
|  | AGENT_CODE | varchar(20) | 20 | NULL allowed | _Agent Code. Always null for Subscribers_ |
|  | CREATION_TYPE | varchar(1) | 1 | NULL allowed | _Subsriber user created with a Type (B or M)_ |
|  | BULK_ID | varchar(20) | 20 | NULL allowed | _Identifier of the bulk treatment, when subscriber has been registered/modified by  a batch bulk treatment. Useful to recognize subscribers who have been registered/modified by the same batch._ |
|  | IDENTITY_PROOF_TYPE | varchar(60) | 60 | NULL allowed | _type of document that has been scanned for the identity proof (document available on the Tango server). NATIONAL_ID, VOTER_CARD, NA, DRIVER_CARD, PASSPORT..._ |
|  | ADDRESS_PROOF_TYPE | varchar(60) | 60 | NULL allowed | _type of document that has been scanned for the identity proof (document available on the Tango server). NATIONAL_ID, VOTER_CARD, NA, DRIVER_CARD, PASSPORT..._ |
|  | PHOTO_PROOF_TYPE | varchar(60) | 60 | NULL allowed | _type of document that has been scanned for the identity proof (document available on the Tango server). NATIONAL_ID, VOTER_CARD, NA, DRIVER_CARD, PASSPORT..._ |
|  | ID_TYPE | varchar(20) | 20 | NULL allowed | _ID Type. NATIONAL_ID, PAN_CARD, VOTER_CARD, RATION_CARD, GOVT_ ID, PASSPORT, DRIVER_CARD, SSN..._ |
|  | ID_NO | varchar(20) | 20 | NULL allowed | _ID No_ |
|  | ID_ISSUE_PLACE | varchar(30) | 30 | NULL allowed | _Place of Issue_ |
|  | ID_ISSUE_DATE | datetime | 8 | NULL allowed | _ID Issue Date_ |
|  | ID_ISSUE_COUNTRY | varchar(40) | 40 | NULL allowed | _ID Issue Country (code of the country, and not full name)_ |
|  | ID_EXPIRY_DATE | datetime | 8 | NULL allowed | _ID Expiry Date_ |
|  | RESIDENCE_COUNTRY | varchar(40) | 40 | NULL allowed | _Resisdent Country (code of the country, and not full name)_ |
|  | NATIONALITY | varchar(80) | 80 | NULL allowed | _Nationality_ |
|  | EMPLOYER_NAME | varchar(80) | 80 | NULL allowed | _Name of the Employer_ |
|  | POSTAL_CODE | varchar(20) | 20 | NULL allowed | _Postal Code_ |
|  | SOUSCRIPTION_TYPE | varchar(20) | 20 | NULL allowed | _This field will identify, if the subscriber is created via WEB TANGO, BULK import or NOMAD/USSD souscription. BULK or NOMAD/USSD or WEB TANGO_ |
|  | MOBILE_GROUP_ROLE | varchar(38) | 38 | NULL allowed | _Group role of the subscribers PRIMARY wallet. See the GroupeRoles export content_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Compression | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Subscribers_V11: *](../../../../Images/pkcluster.png)](#indexes) | PK_Subscribers_V11 | FileID, ID, RefDate | YES | PAGE ON PARTITIONS (1), PAGE ON PARTITIONS (2), PAGE ON PARTITIONS (3), PAGE ON PARTITIONS (4), PAGE ON PARTITIONS (5), PAGE ON PARTITIONS (6), PAGE ON PARTITIONS (7), PAGE ON PARTITIONS (8), PAGE ON PARTITIONS (9), PAGE ON PARTITIONS (10), PAGE ON PARTITIONS (11), PAGE ON PARTITIONS (12), PAGE ON PARTITIONS (13) | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

