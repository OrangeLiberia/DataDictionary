#### 

[Project](../../../../../index.md) > [192.168.19.120\\BI](../../../../index.md) > [User databases](../../../index.md) > [BI](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > fwk.spt_ETLRun

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [fwk].[spt_ETLRun]

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) | Direction |
|---|---|---|---|
| @DayToProcess | datetime | 8 |  |
| @IN | bit | 1 |  |
| @MSC | bit | 1 |  |
| @Extract | bit | 1 |  |
| @Transform | bit | 1 |  |
| @Load | bit | 1 |  |
| @Subs | bit | 1 |  |
| @Calls | bit | 1 |  |
| @Transactions | bit | 1 |  |
| @ForceYM | bit | 1 |  |
| @SendReports | bit | 1 |  |
| @ExecMode | tinyint | 1 |  |
| @IDETLRun | bigint | 8 | Out |
| @StartEngine | bit | 1 |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

