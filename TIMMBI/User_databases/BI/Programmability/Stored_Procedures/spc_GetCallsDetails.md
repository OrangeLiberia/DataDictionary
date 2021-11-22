#### 

[Project](../../../../../index.md) > [192.168.19.120\\BI](../../../../index.md) > [User databases](../../../index.md) > [BI](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > in.spc_GetCallsDetails

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [in].[spc_GetCallsDetails]

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Day | datetime | 8 |
| @CallType | varchar(10) | 10 |
| @WalletID | int | 4 |
| @IDOrig | int | 4 |
| @IDDest | int | 4 |
| @OnlySuccessCalls | bit | 1 |
| @OnlyChargedCalls | bit | 1 |
| @Top | int | 4 |
| @Debug | bit | 1 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

