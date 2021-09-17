#### 

[Project](../../../../../index.md) > [192.168.19.40\\ERIS](../../../../index.md) > [User databases](../../../index.md) > [SIMRegistration](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > dbo.sps_SIMRegistrationAttempt

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [dbo].[sps_SIMRegistrationAttempt]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @MSISDN | varchar(20) | 20 |
| @APP | varchar(10) | 10 |
| @FullName | varchar(150) | 150 |
| @FirstName | varchar(50) | 50 |
| @MiddleName | varchar(50) | 50 |
| @LastName | varchar(50) | 50 |
| @Gender | varchar(20) | 20 |
| @IDCard | varchar(20) | 20 |
| @IDCardType | varchar(50) | 50 |
| @BirthDate | datetime | 8 |
| @BirthPlace | varchar(50) | 50 |
| @MaritalStatus | varchar(20) | 20 |
| @AddressType | varchar(20) | 20 |
| @Address | varchar(200) | 200 |
| @AddressCounty | varchar(30) | 30 |
| @Country | varchar(50) | 50 |
| @EMail | varchar(100) | 100 |
| @Job | varchar(50) | 50 |
| @ConfirmationCode | varchar(5) | 5 |
| @FrontPicture | image | 16 |
| @FrontPictureFile | varchar(100) | 100 |
| @IDCardPicture | image | 16 |
| @IDCardPictureFile | varchar(100) | 100 |
| @ContractPicture | image | 16 |
| @ContractPictureFile | varchar(100) | 100 |
| @AgentUserName | varchar(20) | 20 |
| @AgentID | int | 4 |
| @MobileMoney | bit | 1 |
| @RegistrationDate | datetime | 8 |
| @AppVersion | varchar(10) | 10 |
| @NextOfKinName | varchar(150) | 150 |
| @NextOfKinPhoneNumber | varchar(20) | 20 |
| @NextOfKinEmail | varchar(100) | 100 |
| @AgentMSISDN | varchar(20) | 20 |
| @AgentIMEI | varchar(20) | 20 |
| @AgentICCID | varchar(20) | 20 |
| @GPSLocation | varchar(50) | 50 |
| @ExecuteImmediately | bit | 1 |
| @StandBy | bit | 1 |
| @ResultSet | bit | 1 |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

