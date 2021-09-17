#### 

[Project](../../../../../index.md) > [192.168.19.40\\ERIS](../../../../index.md) > [User databases](../../../index.md) > [SIMRegistration](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > dbo.sps_GetSIMRegistrationInfo

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [dbo].[sps_GetSIMRegistrationInfo]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) | Direction |
|---|---|---|---|
| @ID | bigint | 8 |  |
| @MSISDN | varchar(20) | 20 |  |
| @ResultSet | bit | 1 |  |
| @FullName | varchar(200) | 200 | Out |
| @Gender | varchar(20) | 20 | Out |
| @IDCard | varchar(20) | 20 | Out |
| @IDCardType | varchar(50) | 50 | Out |
| @BirthDate | datetime | 8 | Out |
| @BirthPlace | varchar(50) | 50 | Out |
| @MaritalStatus | varchar(20) | 20 | Out |
| @AddressType | varchar(20) | 20 | Out |
| @Address | varchar(200) | 200 | Out |
| @AddressCounty | varchar(30) | 30 | Out |
| @EMail | varchar(200) | 200 | Out |
| @Job | varchar(50) | 50 | Out |
| @Country | varchar(50) | 50 | Out |
| @RegistrationDate | datetime | 8 | Out |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

