#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.SIMRegistrationBuffer

# ![Tables](../../../../Images/Table32.png) [dbo].[SIMRegistrationBuffer]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrationBuffer: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_SIMRegistrationBuffer_MSISDN](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |  |  |
| [![Check Constraints CHK_SimRegBuff_APP : ([APP]='MIG' OR [APP]='TEST' OR [APP]='SIMREG' OR [APP]='SMSREG' OR [APP]='TIMM-OS' OR [APP]='TIMM-CC')](../../../../Images/c-constraint.png)](#checkconstraints) | APP | varchar(10) | 10 | NOT NULL |  |  |
|  | ExecState | smallint | 2 | NOT NULL |  | ((0)) |
|  | ReturnID | smallint | 2 | NULL allowed |  | ((0)) |
|  | SubsID | numeric(18,0) | 9 | NULL allowed |  |  |
|  | TIMMAccaoID | numeric(18,0) | 9 | NULL allowed |  |  |
|  | TIMMTipoAccao | varchar(50) | 50 | NULL allowed |  |  |
|  | NTIMMPics | int | 4 | NULL allowed |  |  |
|  | FullName | varchar(150) | 150 | NULL allowed |  |  |
|  | FirstName | varchar(50) | 50 | NULL allowed |  |  |
|  | MiddleName | varchar(50) | 50 | NULL allowed |  |  |
|  | LastName | varchar(50) | 50 | NULL allowed |  |  |
|  | BirthDate | datetime | 8 | NULL allowed |  |  |
|  | BirthPlace | varchar(50) | 50 | NULL allowed |  |  |
|  | Gender | varchar(20) | 20 | NULL allowed |  |  |
|  | MaritalStatus | varchar(20) | 20 | NULL allowed |  |  |
|  | IDCard | varchar(20) | 20 | NULL allowed |  |  |
|  | IDCardType | varchar(20) | 20 | NULL allowed |  |  |
|  | IDFrontPicture | bigint | 8 | NULL allowed |  |  |
|  | IDCardPicture | bigint | 8 | NULL allowed |  |  |
|  | IDContractPicture | bigint | 8 | NULL allowed |  |  |
|  | AddressType | varchar(20) | 20 | NULL allowed |  |  |
|  | AddressCounty | varchar(30) | 30 | NULL allowed |  |  |
|  | Address | varchar(150) | 150 | NULL allowed |  |  |
|  | EMail | varchar(100) | 100 | NULL allowed |  |  |
|  | Job | varchar(50) | 50 | NULL allowed |  |  |
|  | Country | varchar(50) | 50 | NULL allowed |  |  |
|  | ConfirmationCode | varchar(10) | 10 | NULL allowed |  |  |
|  | RegistrationDate | datetime | 8 | NULL allowed |  |  |
| [![Indexes IX_SIMRegistrationBuffer_MSISDN](../../../../Images/Index.png)](#indexes) | EntryDate | datetime | 8 | NOT NULL |  | (getdate()) |
|  | DownloadDate | datetime | 8 | NULL allowed |  |  |
|  | ExecutionDate | datetime | 8 | NULL allowed |  |  |
|  | AgentID | int | 4 | NULL allowed |  |  |
|  | AgentUserName | varchar(20) | 20 | NULL allowed |  |  |
|  | AppVersion | varchar(10) | 10 | NULL allowed |  |  |
|  | AgentMSISDN | varchar(20) | 20 | NULL allowed |  |  |
|  | AgentIMEI | varchar(20) | 20 | NULL allowed |  |  |
|  | AgentICCID | varchar(20) | 20 | NULL allowed |  |  |
|  | GPSLocation | varchar(50) | 50 | NULL allowed |  |  |
|  | CellID | int | 4 | NULL allowed |  |  |
|  | MobileMoney | bit | 1 | NULL allowed |  |  |
|  | NextOfKinName | varchar(150) | 150 | NULL allowed |  |  |
|  | NextOfKinPhoneNumber | varchar(20) | 20 | NULL allowed |  |  |
|  | NextOfKinEmail | varchar(100) | 100 | NULL allowed |  |  |
|  | MobileMoneyApp | varchar(10) | 10 | NULL allowed |  |  |
|  | MobileMoneyID | varchar(100) | 100 | NULL allowed |  |  |
|  | MobileMoneyMsg | varchar(max) | max | NULL allowed |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrationBuffer: ID](../../../../Images/pkcluster.png)](#indexes) | PK_SIMRegistrationBuffer | ID | YES |
|  | IX_SIMRegistrationBuffer_MSISDN | MSISDN, EntryDate |  |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

