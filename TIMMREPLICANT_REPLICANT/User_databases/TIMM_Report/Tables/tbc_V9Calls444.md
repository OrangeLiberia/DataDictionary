#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9Calls444

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9Calls444]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 40265146 |
| Created | 1:35:08 PM Tuesday, March 24, 2020 |
| Last Modified | 1:35:08 PM Tuesday, March 24, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| MSISDN | varchar(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| Destination | varchar(20) | 20 | NOT NULL | _Destination type_ |
| ANSWER_TIME | datetime | 8 | NOT NULL | _Inicial time of the call_ |
| DISCONNECT_TIME | datetime | 8 | NOT NULL | _End time of the call_ |
| CHARGEABLE_DURATION | int | 4 | NULL allowed | _Duration of the call rounded_ |
| AMOUNT_CHARGED | decimal(18,6) | 9 | NULL allowed | _Amount charged_ |


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

## <a name="#usedby"></a>Used By

* [dbo].[spc_444DailyCalls]
* [dbo].[spc_Process444CallsV9]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

