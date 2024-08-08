#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9DataTransferSubs

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9DataTransferSubs]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 401793 |
| Created | 4:47:43 PM Monday, February 24, 2020 |
| Last Modified | 4:47:43 PM Monday, February 24, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| MSISDNDonor | char(9) | 9 | NOT NULL | _MSISDN of the Donor_ |
| MSISDNReceiver | char(9) | 9 | NOT NULL | _MSISDN of the Receiver_ |
| MB | bigint | 8 | NULL allowed | _Total of MB_ |


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

* [dbo].[spc_ProcessV9DataTransfer]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

