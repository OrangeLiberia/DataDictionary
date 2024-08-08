#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.BundleDR_Dup

# ![Tables](../../../../Images/Table32.png) [dbo].[BundleDR_Dup]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 27543 |
| Created | 3:31:08 PM Thursday, November 19, 2020 |
| Last Modified | 3:31:08 PM Thursday, November 19, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| FileID | bigint | 8 | NOT NULL |  |
| CDRID | int | 4 | NOT NULL |  |
| RefFileDate | date | 3 | NULL allowed |  |
| BUNDLE_ID | bigint | 8 | NULL allowed |  |
| SUBS_NUMBER | varchar(32) | 32 | NULL allowed |  |
| EVENT_DATE | datetime | 8 | NULL allowed | _Date and time of the event_ |
| ACTIVATION_DATE | datetime | 8 | NULL allowed | _Date and time of the Bundle Activation_ |
| ACTION | bigint | 8 | NULL allowed | _8 - activation, 24 - deactivation_ |
| EXPIRATION_DATE | datetime | 8 | NULL allowed | _Date and time of the Bundle deactivation_ |
| COS_ID | int | 4 | NULL allowed | _IN COS ID of the Subscriber_ |


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

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

