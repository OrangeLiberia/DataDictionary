#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_ShortcodesCDRsConfig_Report_Subscription

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_ShortcodesCDRsConfig_Report_Subscription]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 23 |
| Created | 11:52:35 AM Friday, May 15, 2020 |
| Last Modified | 12:09:18 PM Friday, February 19, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbc_ShortcodesCDRsConfig_Report_Subscription: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Name | varchar(32) | 32 | NOT NULL |  | _Name_ |
|  | Subject | varchar(1000) | 1000 | NOT NULL |  |  |
|  | Recipients | varchar(1000) | 1000 | NOT NULL |  |  |
|  | CopyRecipients | varchar(1000) | 1000 | NULL allowed |  |  |
|  | BlindCopyRecipients | varchar(1000) | 1000 | NULL allowed |  |  |
|  | ReplyTo | varchar(1000) | 1000 | NULL allowed |  |  |
|  | Status | int | 4 | NOT NULL |  |  |
|  | SendEmpty | bit | 1 | NOT NULL |  |  |
|  | Grouped | smallint | 2 | NULL allowed |  |  |
|  | ReportCDR | tinyint | 1 | NULL allowed |  |  |


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

