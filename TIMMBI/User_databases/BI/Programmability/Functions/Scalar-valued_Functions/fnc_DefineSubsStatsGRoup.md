#### 

[Project](../../../../../../index.md) > [192.168.19.120\\BI](../../../../../index.md) > [User databases](../../../../index.md) > [BI](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Scalar-valued Functions](Scalar-valued_Functions.md) > crm.fnc_DefineSubsStatsGRoup

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [crm].[fnc_DefineSubsStatsGRoup]

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Type | varchar(10) | 10 |
| @BIActivityDuringTF | bit | 1 |
| @BIActivityBeforeTF | bit | 1 |
| @BIFirstActivity | datetime | 8 |
| @BILastActivity | datetime | 8 |
| @PreActDate | datetime | 8 |
| @StatusChangedDuringTF | int | 4 |
| @TipoCartaoID | int | 4 |
| @TIMMRegistered | tinyint | 1 |
| @FakeReg | tinyint | 1 |
| @DataValid | int | 4 |
| @NPics | int | 4 |
| @DataService | tinyint | 1 |
| @Protected | tinyint | 1 |
| @Corporate | bit | 1 |
| @PrePos | varchar(3) | 3 |
| @ICCID | varchar(18) | 18 |
| @DT1YearAgo | date | 3 |
| @ValidGSM | tinyint | 1 |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | EXECUTE | TIMM\\BU-Marketing |
| Grant | EXECUTE | TIMM\\BU-Sales |
| Grant | EXECUTE | olib_bu_sales |
| Grant | EXECUTE | TIMM\\BU-Finance |
| Grant | EXECUTE | olib_bu_finance |
| Grant | EXECUTE | TIMM\\BU-MIS-ADD |
| Grant | EXECUTE | olib_bu_mis_add |
| Grant | EXECUTE | TIMM\\BU-OrangeMoney |
| Grant | EXECUTE | olib_bu_orangemoney |
| Grant | EXECUTE | olib_bu_marketing |
| Grant | VIEW DEFINITION | TIMM\\BU-Marketing |
| Grant | VIEW DEFINITION | TIMM\\BU-Sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | VIEW DEFINITION | TIMM\\BU-Finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | VIEW DEFINITION | TIMM\\BU-MIS-ADD |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | VIEW DEFINITION | TIMM\\BU-OrangeMoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

