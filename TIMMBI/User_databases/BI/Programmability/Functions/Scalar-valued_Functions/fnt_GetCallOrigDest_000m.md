#### 

[Project](../../../../../../index.md) > [TIMMBI\\BI](../../../../../index.md) > [User databases](../../../../index.md) > [BI](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Scalar-valued Functions](Scalar-valued_Functions.md) > msc.fnt_GetCallOrigDest

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [msc].[fnt_GetCallOrigDest]

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Type | varchar(10) | 10 |
| @TrunkOut | varchar(10) | 10 |
| @OrigMSISDN | varchar(20) | 20 |
| @OrigNDC | varchar(6) | 6 |
| @OrigCC | varchar(6) | 6 |
| @TrunkIn | varchar(10) | 10 |
| @TermMSISDN | varchar(20) | 20 |
| @TermNDC | varchar(6) | 6 |
| @TermCC | varchar(6) | 6 |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | EXECUTE | Reader |
| Grant | EXECUTE | olib_bu_sales |
| Grant | EXECUTE | olib_bu_finance |
| Grant | EXECUTE | olib_bu_mis_add |
| Grant | EXECUTE | olib_bu_orangemoney |
| Grant | EXECUTE | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

