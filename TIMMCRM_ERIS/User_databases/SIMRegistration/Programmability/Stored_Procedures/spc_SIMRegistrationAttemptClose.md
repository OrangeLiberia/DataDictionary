#### 

[Project](../../../../../index.md) > [192.168.19.40\\ERIS](../../../../index.md) > [User databases](../../../index.md) > [SIMRegistration](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > dbo.spc_SIMRegistrationAttemptClose

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [dbo].[spc_SIMRegistrationAttemptClose]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @ClientID | numeric(18,0) | 9 |
| @AccountID | numeric(18,0) | 9 |
| @SubsID | numeric(18,0) | 9 |
| @RegistrationDate | datetime | 8 |
| @IDSimReg | bigint | 8 |
| @Registered | bit | 1 |
| @CurrentRegistrationDate | datetime | 8 |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

