#### 

[Project](../../../../../index.md) > [192.168.19.40\\ERIS](../../../../index.md) > [User databases](../../../index.md) > [SIMRegistration](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > dbo.sps_SIMRegistrationAttemptXML

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [dbo].[sps_SIMRegistrationAttemptXML]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @RegistrationData | varchar(max) | max |
| @FrontPicture | image | 16 |
| @IDCardPicture | image | 16 |
| @ContractPicture | image | 16 |
| @AgentID | int | 4 |
| @APP | varchar(10) | 10 |
| @ExecuteImmediately | bit | 1 |
| @StandBy | bit | 1 |
| @ResultSet | bit | 1 |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

