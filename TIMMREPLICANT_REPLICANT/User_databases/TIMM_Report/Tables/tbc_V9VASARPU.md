#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9VASARPU

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9VASARPU]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 16794 |
| Created | 9:31:31 PM Wednesday, December 25, 2019 |
| Last Modified | 9:31:31 PM Wednesday, December 25, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_V9VASARPU: ReferenceDay\TDRID](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Primary Key PK_tbc_V9VASARPU: ReferenceDay\TDRID](../../../../Images/pk.png)](#indexes) | TDRID | int | 4 | NOT NULL | _ID of the TDR (see [dbo.tbc_TDRID](tbc_TDRID.md))_ |
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

## <a name="#usedby"></a>Used By

* [dbo].[spc_ProcessV9VAS]
* [dbo].[spc_VASDailyARPU]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

