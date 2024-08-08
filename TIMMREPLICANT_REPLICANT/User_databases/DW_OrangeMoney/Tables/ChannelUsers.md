#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.ChannelUsers

# ![Tables](../../../../Images/Table32.png) [dbo].[ChannelUsers]

---

## <a name="#description"></a>MS_Description

Contains the list of channel-users, operators and merchants that has been created, deleted, or modified.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  | _Unique File Identifier_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL |  | _Unique Data Line within a file_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | (getdate()) | _Date of the file_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CurrencyType | varchar(16) | 16 | NOT NULL |  | _Currency (USD/LRD)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_User_Details](../../../../Images/Index.png)](#indexes) | USERID | varchar(20) | 20 | NULL allowed |  |  |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | PROFILE_ID | varchar(20) | 20 | NULL allowed |  | _Id of the Profile assigned to PRIMARY WALLET of the user.A profile is a set of thresholds applied to the Orange Money user (maximum amounts and numbers of transactions per day, week, month, etc.)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | PARENT_ID | varchar(20) | 20 | NULL allowed |  | _User_id of the users parent (for distributors hierarchy)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | PARENT_USER_MSISDN | varchar(15) | 15 | NULL allowed |  | _MSISDN if the users parent_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | MSISDN | varchar(15) | 15 | NULL allowed |  | _MSISDN of the user (user mobile number)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | USER_NAME_PREFIX | varchar(100) | 100 | NULL allowed |  | _Prefix to apply to the user name _ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_User_Details](../../../../Images/Index.png)](#indexes) | USERNAME | varchar(80) | 80 | NULL allowed |  | _Username_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | LAST_NAME | varchar(80) | 80 | NULL allowed |  | _Last name of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | SHORT_NAME | varchar(15) | 15 | NULL allowed |  | _Short name of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | DOB | varchar(50) | 50 | NULL allowed |  | _Date of birth of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | REGISTERED_ON | datetime | 8 | NULL allowed |  | _Date of the users registration_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ADDRESS1 | varchar(50) | 50 | NULL allowed |  | _Address1 of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ADDRESS2 | varchar(50) | 50 | NULL allowed |  | _Address2 of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | STATE | varchar(30) | 30 | NULL allowed |  | _Value of the state field of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CITY | varchar(30) | 30 | NULL allowed |  | _City of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | COUNTRY | varchar(20) | 20 | NULL allowed |  | _Country of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | SSN | varchar(15) | 15 | NULL allowed |  | _Value of the SSN field of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | DESIGNATION | varchar(30) | 30 | NULL allowed |  | _Value of the Designation field of the Channel or Operator User.This field can be used to recognize special users (transactions of these specific users can then be count separately, cf. specifications of transaction TAGS)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | DIVISION | varchar(30) | 30 | NULL allowed |  | _Value of the Division field of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CONTACT_PERSON | varchar(80) | 80 | NULL allowed |  | _Contact_person for the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CONTACT_NO | varchar(50) | 50 | NULL allowed |  | _Contact number for the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | EMPLOYEE_CODE | varchar(12) | 12 | NULL allowed |  | _Employee_code of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | SEX | varchar(10) | 10 | NULL allowed |  | _Gender of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_NUMBER | varchar(40) | 40 | NULL allowed |  | _External code of the user (used to store the number of the users identity card)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | E_MAIL | varchar(60) | 60 | NULL allowed |  | _E_mail address of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | WEB_LOGIN | varchar(20) | 20 | NULL allowed |  | _Login of the user for his tango web access_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | STATUS | varchar(2) | 2 | NULL allowed |  | _Status of the user : Y = Activated, S = Suspended, N = Deleted (Deteted means : deactivated with no possibility to reactivate)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CREATION_ON | datetime | 8 | NULL allowed |  | _Date of the users creation (same date than in field registered_on)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CREATED_BY | varchar(20) | 20 | NULL allowed |  | _User_id of the user that have registered the user._ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CREATED_BY_MSISDN | varchar(15) | 15 | NULL allowed |  | _MSISDN of the user that have registered the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | NOMADE_CREATED_BY | varchar(10) | 10 | NULL allowed |  | _No Nomad/USSD registration for Channel, Merchant and Operator users_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | LEVEL1_APPROVED_ON | datetime | 8 | NULL allowed |  | _Date of the first level of approval of the users activation_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | LEVEL1_APPROVED_BY | varchar(30) | 30 | NULL allowed |  | _user_id of the Orange Money user who has validated the users activation at the first level of approval_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | LEVEL2_APPROVED_ON | datetime | 8 | NULL allowed |  | _Date of the second/last level of approval of the users activation_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | LEVEL2_APPROVED_BY | varchar(30) | 30 | NULL allowed |  | _user_id of the Orange Money user who has validated the users activation at the second/last level of approval_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | OWNER_ID | varchar(20) | 20 | NULL allowed |  | _User_id of the users owner_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | OWNER_MSISDN | varchar(15) | 15 | NULL allowed |  | _MSISDN of the users owner_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_User_Details](../../../../Images/Index.png)](#indexes) | USER_DOMAIN_CODE | varchar(10) | 10 | NULL allowed |  | _Domain code of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_User_Details](../../../../Images/Index.png)](#indexes) | CATEGORY_CODE | varchar(10) | 10 | NULL allowed |  | _Code of the users category_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | USER_GRADE_NAME | varchar(40) | 40 | NULL allowed |  | _Name (and not code) of the user grade_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | MODIFIED_BY | varchar(30) | 30 | NULL allowed |  | _User_id of the user that have done the last users data modification_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | MODIFIED_ON | datetime | 8 | NULL allowed |  | _Date of the last users data modification_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | MODIFY_APPROVED_BY | varchar(25) | 25 | NULL allowed |  | _User_id of the user that have approved the last users data modification_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | MODIFIED_APPROVED_ON | datetime | 8 | NULL allowed |  | _Date of approval of the last users data modification_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | DELETED_ON | datetime | 8 | NULL allowed |  | _Date of users deletion approval_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | DEACTIVATION_BY | varchar(50) | 50 | NULL allowed |  | _User_id of the Operator user that have approved the user deletion_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | DEPARTMENT | varchar(30) | 30 | NULL allowed |  | _Value of the Department field of the Operator user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | REG_FORM_NUM | varchar(20) | 20 | NULL allowed |  | _Form number used for the users registration_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | REMARKS | varchar(100) | 100 | NULL allowed |  | _Value of the Remarks field of the Channel or Merchant User_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_User_Details](../../../../Images/Index.png)](#indexes) | GEOGRAPHICAL_DOMAIN | varchar(50) | 50 | NULL allowed |  | _Geographical domain name of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | GROUP_ROLE | varchar(35) | 35 | NULL allowed |  | _Group Role ID assigned to the Channel or Operator User _ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | FIRST_TRANSACTION_ON | datetime | 8 | NULL allowed |  | _Date of the first transaction TS of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes)[![Indexes IX_User_Details](../../../../Images/Index.png)](#indexes) | COMPANY_CODE | varchar(15) | 15 | NULL allowed |  | _When the user is a MERCHANT user, this field contains the code of represented billing company, otherwise it is empty_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | USER_TYPE | varchar(10) | 10 | NULL allowed |  | _User type_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ACTION_TYPE | varchar(20) | 20 | NULL allowed |  | _This field indicates wether the User is logged because of its creation, activation, desactivation or modification. Indeed, this field contains the value CREATION, ACTIVATION, DESACTIVATION or MODIFICATION according to the following rules:<br />- value CREATION when the logged user is a new one (registered on the day targetted by the data extraction)<br />- value ACTIVATION when the user registration has been validated on the day targetted by the data extraction (no such validation for user, this rule only applies to Channel Users).<br />- value DESACTIVATION when the user has been deleted on the day targetted by the data extraction.<br />- value MODIFICATION when the user has already been logged when created (on a previous day), but has been modified on the day targetted by the data extraction.<br />- value CREATION_DESACT when the user has been created and then deleted on the day targetted by the data extraction.<br />- value ACTIVATION_DESACT when the user registration has been validated and then the user deleted on the day targetted by the data extraction_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | AGENT_CODE | varchar(20) | 20 | NULL allowed |  | _Code of the channel users, that should be used by the subscribers for one step transactions (for example one step merchant payment or one step cashout)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | CREATION_TYPE | varchar(1) | 1 | NULL allowed |  | _Channel User, or Operator User created with a Type (B or M)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | BULK_ID | varchar(20) | 20 | NULL allowed |  | _Identifier of the bulk treatment, when the channel user has been registered/modified by  a batch bulk treatment. Useful to recognize users who have been registered/modified by the same batch._ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | IDENTITY_PROOF_TYPE | varchar(60) | 60 | NULL allowed |  | _type of document that has been scanned for the identity proof (document available on the Tango server)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ADDRESS_PROOF_TYPE | varchar(60) | 60 | NULL allowed |  | _type of document that has been scanned for the identity proof (document available on the Tango server)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | PHOTO_PROOF_TYPE | varchar(60) | 60 | NULL allowed |  | _type of document that has been scanned for the identity proof (document available on the Tango server)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_TYPE | varchar(20) | 20 | NULL allowed |  | _ID Type_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_NO | varchar(20) | 20 | NULL allowed |  | _ID No_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_ISSUE_PLACE | varchar(30) | 30 | NULL allowed |  | _Place of Issue_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_ISSUE_DATE | datetime | 8 | NULL allowed |  | _ID Issue Date_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_ISSUE_COUNTRY | varchar(40) | 40 | NULL allowed |  | _ID Issue Country_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | ID_EXPIRY_DATE | datetime | 8 | NULL allowed |  | _ID Expiry Date_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | RESIDENCE_COUNTRY | varchar(40) | 40 | NULL allowed |  | _Resisdent Country_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | NATIONALITY | varchar(80) | 80 | NULL allowed |  | _Nationality_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | EMPLOYER_NAME | varchar(80) | 80 | NULL allowed |  | _Name of the Employer_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | POSTAL_CODE | varchar(20) | 20 | NULL allowed |  | _Postal Code_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | SOUSCRIPTION_TYPE | varchar(20) | 20 | NULL allowed |  | _This field will identify, if the subscriber is created via (WEB TANGO,BULK or USSD)_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | MOBILE_GROUP_ROLE | varchar(38) | 38 | NULL allowed |  | _Group role of the PRIMARY wallet of the user_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | LAST_LOGIN_ON | varchar(96) | 96 | NULL allowed |  | _Date of the last login_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | USER_GRADE_CODE | varchar(96) | 96 | NULL allowed |  | _User grade_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | PARENT_FIRST_NAME | varchar(96) | 96 | NULL allowed |  | _Parent's first name_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | PARENT_LAST_NAME | varchar(96) | 96 | NULL allowed |  | _Parent's last name_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | OWNER_FIRST_NAME | varchar(96) | 96 | NULL allowed |  | _Owner first name_ |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | OWNER_LAST_NAME | varchar(96) | 96 | NULL allowed |  | _Owner last name_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|---|
|  | IX_User_Details | USERNAME, USERID, USER_DOMAIN_CODE, GEOGRAPHICAL_DOMAIN, CATEGORY_CODE, COMPANY_CODE |  |  |  |  |  | pschSemesterPartition | RefDate |
| [![Cluster Key cci_ChannelUsers: *](../../../../Images/cluster.png)](#indexes) | cci_ChannelUsers |  | FileID, ID, RefDate, CurrencyType, USERID, PROFILE_ID, PARENT_ID, PARENT_USER_MSISDN, MSISDN, USER_NAME_PREFIX, USERNAME, LAST_NAME, SHORT_NAME, DOB, REGISTERED_ON, ADDRESS1, ADDRESS2, STATE, CITY, COUNTRY, SSN, DESIGNATION, DIVISION, CONTACT_PERSON, CONTACT_NO, EMPLOYEE_CODE, SEX, ID_NUMBER, E_MAIL, WEB_LOGIN, STATUS, CREATION_ON, CREATED_BY, CREATED_BY_MSISDN, NOMADE_CREATED_BY, LEVEL1_APPROVED_ON, LEVEL1_APPROVED_BY, LEVEL2_APPROVED_ON, LEVEL2_APPROVED_BY, OWNER_ID, OWNER_MSISDN, USER_DOMAIN_CODE, CATEGORY_CODE, USER_GRADE_NAME, MODIFIED_BY, MODIFIED_ON, MODIFY_APPROVED_BY, MODIFIED_APPROVED_ON, DELETED_ON, DEACTIVATION_BY, DEPARTMENT, REG_FORM_NUM, REMARKS, GEOGRAPHICAL_DOMAIN, GROUP_ROLE, FIRST_TRANSACTION_ON, COMPANY_CODE, USER_TYPE, ACTION_TYPE, AGENT_CODE, CREATION_TYPE, BULK_ID, IDENTITY_PROOF_TYPE, ADDRESS_PROOF_TYPE, PHOTO_PROOF_TYPE, ID_TYPE, ID_NO, ID_ISSUE_PLACE, ID_ISSUE_DATE, ID_ISSUE_COUNTRY, ID_EXPIRY_DATE, RESIDENCE_COUNTRY, NATIONALITY, EMPLOYER_NAME, POSTAL_CODE, SOUSCRIPTION_TYPE, MOBILE_GROUP_ROLE, LAST_LOGIN_ON, USER_GRADE_CODE, PARENT_FIRST_NAME, PARENT_LAST_NAME, OWNER_FIRST_NAME, OWNER_LAST_NAME | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

