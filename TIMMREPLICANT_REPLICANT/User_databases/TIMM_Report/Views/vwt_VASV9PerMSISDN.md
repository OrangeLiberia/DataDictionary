#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Views](Views.md) > dbo.vwt_VASV9PerMSISDN

# ![Views](../../../../Images/View32.png) [dbo].[vwt_VASV9PerMSISDN]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Schema Bound | YES |
| Created | 9:46:34 PM Thursday, January 16, 2020 |
| Last Modified | 1:35:20 PM Friday, December 11, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Day | char(10) | 10 |
| MSISDN | char(9) | 9 |
| TDRID | int | 4 |
| VAS | varchar(100) | 100 |
| Value | decimal(38,6) | 17 |
| Activations | int | 4 |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | SELECT | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | SELECT | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | SELECT | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | SELECT | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | SELECT | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

## <a name="#uses"></a>Uses

* [[dbo].[tbc_TDRID]](../Tables/tbc_TDRID.md)
* [[dbo].[tbc_V9VASSubAct]](../Tables/tbc_V9VASSubAct.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

