#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.POS_Users

# ![Tables](../../../../Images/Table32.png) [dbo].[POS_Users]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 65 |
| Created | 10:08:11 AM Tuesday, April 6, 2021 |
| Last Modified | 10:08:11 AM Tuesday, April 6, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ID_Number | varchar(50) | 50 | NOT NULL |
| Name | nvarchar(50) | 100 | NOT NULL |
| Channel | nvarchar(50) | 100 | NOT NULL |
| Sub_Channel | nvarchar(50) | 100 | NULL allowed |
| Area_Of_Working | nvarchar(50) | 100 | NOT NULL |
| Status_of_Agent | nvarchar(50) | 100 | NULL allowed |


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

