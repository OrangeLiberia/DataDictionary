#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_GlobalPassReportARPU

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_GlobalPassReportARPU]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 0 |
| Created | 12:33:45 PM Tuesday, February 4, 2020 |
| Last Modified | 12:33:45 PM Tuesday, February 4, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_GlobalPassReportARPU: ReferenceDay](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
|  | ARPU0_5 | int | 4 | NULL allowed | _Total subscribers on ARPU range [0-5[_ |
|  | ARPU5_10 | int | 4 | NULL allowed | _Total subscribers on ARPU range [5-10[_ |
|  | ARPU10_20 | int | 4 | NULL allowed | _Total subscribers on ARPU range [10-20[_ |
|  | ARPU20_50 | int | 4 | NULL allowed | _Total subscribers on ARPU range [20-50[_ |
|  | ARPUPlus50 | int | 4 | NULL allowed | _Total subscribers on ARPU range 50 plus_ |


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

