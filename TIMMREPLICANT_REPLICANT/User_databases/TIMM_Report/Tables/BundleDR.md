#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.BundleDR

# ![Tables](../../../../Images/Table32.png) [dbo].[BundleDR]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Compression | ROW |
| Row Count (~) | 137659859 |
| Created | 3:19:13 PM Saturday, February 29, 2020 |
| Last Modified | 7:05:44 PM Monday, July 12, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_BundleDR: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_DateBundleQuery](../../../../Images/Index.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_BundleDR: FileID\CDRID](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_DateBundleQuery](../../../../Images/Index.png)](#indexes) | CDRID | int | 4 | NOT NULL |  |
|  | RefFileDate | date | 3 | NULL allowed |  |
| [![Indexes IX_DateBundleQuery](../../../../Images/Index.png)](#indexes) | BUNDLE_ID | bigint | 8 | NULL allowed |  |
|  | SUBS_NUMBER | varchar(32) | 32 | NULL allowed |  |
| [![Indexes IX_DateBundleQuery](../../../../Images/Index.png)](#indexes) | EVENT_DATE | datetime | 8 | NULL allowed | _Date and time of the event_ |
|  | ACTIVATION_DATE | datetime | 8 | NULL allowed | _Date and time of the Bundle Activation_ |
|  | ACTION | bigint | 8 | NULL allowed | _8 - activation, 24 - deactivation_ |
|  | EXPIRATION_DATE | datetime | 8 | NULL allowed | _Date and time of the Bundle deactivation_ |
|  | COS_ID | int | 4 | NULL allowed | _IN COS ID of the Subscriber_ |


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

* [dbo].[spc_MovexDRsV9Campaigns]
* [dbo].[spc_MovexDRsV9CampaignsV2]
* [dbo].[spc_ProcessV9Campaigns]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

