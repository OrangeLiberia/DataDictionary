#### 

[Project](../../../../../index.md) > [192.168.19.40\\ERIS](../../../../index.md) > [User databases](../../../index.md) > [SIMRegistration](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > dbo.sps_SIMRegistrationProv

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [dbo].[sps_SIMRegistrationProv]

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
| @SubsID | numeric(18,0) | 9 |
| @IDSimRegistration | bigint | 8 |
| @Registered | bit | 1 |
| @APP | varchar(10) | 10 |
| @UserID | int | 4 |
| @Corporate | bit | 1 |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

