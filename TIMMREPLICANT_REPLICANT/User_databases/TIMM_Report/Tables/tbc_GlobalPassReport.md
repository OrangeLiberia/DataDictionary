#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_GlobalPassReport

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_GlobalPassReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 0 |
| Created | 12:33:27 PM Tuesday, February 4, 2020 |
| Last Modified | 12:33:45 PM Tuesday, February 4, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key iReferenceDay: ReferenceDay](../../../../Images/cluster.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
|  | ConsumingNumber | varchar(20) | 20 | NULL allowed |  |
|  | BillingParameter2 | varchar(100) | 100 | NULL allowed |  |
| [![Indexes iLocationCode](../../../../Images/Index.png)](#indexes) | LocationCode | varchar(20) | 20 | NULL allowed |  |
|  | ChargeableDuration | int | 4 | NULL allowed |  |
|  | AmountCharged | decimal(18,6) | 9 | NULL allowed | _Amount charged as PAYGO_ |
|  | DialedDigits | char(100) | 100 | NULL allowed |  |
|  | CallingNumber | char(100) | 100 | NULL allowed |  |


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

