#### 

[Project](../../../../../index.md) > [192.168.19.40\\ERIS](../../../../index.md) > [User databases](../../../index.md) > [SIMRegistration](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > dbo.sps_AgentSIMRegistrationStats

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [dbo].[sps_AgentSIMRegistrationStats]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) | Direction |
|---|---|---|---|
| @MSISDN | varchar(20) | 20 |  |
| @IMEI | varchar(20) | 20 |  |
| @ICCID | varchar(20) | 20 |  |
| @AgentID | int | 4 |  |
| @AgentNickName | varchar(50) | 50 |  |
| @Ranking | int | 4 | Out |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

