#### 

[Project](../../../../../index.md) > [192.168.19.120\\BI](../../../../index.md) > [User databases](../../../index.md) > [BI](../../index.md) > [Programmability](../index.md) > [Stored Procedures](Stored_Procedures.md) > fwk.spt_DatabaseBackupAutomatic

# ![Stored Procedures](../../../../../Images/StoredProcedure32.png) [fwk].[spt_DatabaseBackupAutomatic]

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @DatabaseName | varchar(50) | 50 |
| @PathBackup | varchar(200) | 200 |
| @DayToProcess | datetime | 8 |
| @PeriodYMD | char | 1 |
| @DaysOfFullBackup | varchar(100) | 100 |
| @DaysOfDiffBackup | varchar(100) | 100 |
| @DBFilesWithDateTag | bit | 1 |
| @Debug | bit | 1 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

