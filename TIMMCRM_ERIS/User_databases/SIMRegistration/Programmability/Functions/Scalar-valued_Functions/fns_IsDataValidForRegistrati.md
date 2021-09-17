#### 

[Project](../../../../../../index.md) > [192.168.19.40\\ERIS](../../../../../index.md) > [User databases](../../../../index.md) > [SIMRegistration](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Scalar-valued Functions](Scalar-valued_Functions.md) > dbo.fns_IsDataValidForRegistration

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [dbo].[fns_IsDataValidForRegistration]

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
| @FullName | varchar(150) | 150 |
| @FirstName | varchar(50) | 50 |
| @MiddleName | varchar(50) | 50 |
| @LastName | varchar(50) | 50 |
| @Gender | varchar(20) | 20 |
| @BirthDate | datetime | 8 |
| @Address | varchar(200) | 200 |
| @IDCard | varchar(20) | 20 |
| @IDCardType | varchar(50) | 50 |
| @Country | varchar(50) | 50 |
| @Corporate | bit | 1 |
| @NPics | int | 4 |
| @APP | varchar(10) | 10 |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

