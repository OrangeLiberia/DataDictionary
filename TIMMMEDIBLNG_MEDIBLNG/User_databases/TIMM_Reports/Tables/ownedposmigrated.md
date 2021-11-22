#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.ownedposmigrated

# ![Tables](../../../../Images/Table32.png) [dbo].[ownedposmigrated]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 89 |
| Created | 6:53:41 AM Wednesday, February 3, 2021 |
| Last Modified | 11:57:32 AM Monday, February 15, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__ownedpos__3214EC27541A917E: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | PARENT_USER_MSISDN | varchar(10) | 10 | NULL allowed |  |
|  | MSISDN | varchar(10) | 10 | NULL allowed |  |
|  | USER_FIRST_NAME | varchar(100) | 100 | NULL allowed |  |
|  | USER_LAST_NAME | varchar(100) | 100 | NULL allowed |  |
|  | ADDRESS1 | varchar(100) | 100 | NULL allowed |  |
|  | Email | varchar(100) | 100 | NULL allowed |  |
|  | Subject | varchar(200) | 200 | NULL allowed |  |


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

* [TIMM_Report].[dbo].[OMKPIS_OwnStoreBalanceDaily]
* [TIMM_Report].[dbo].[OMKPIS_OwnStoretransactions]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

