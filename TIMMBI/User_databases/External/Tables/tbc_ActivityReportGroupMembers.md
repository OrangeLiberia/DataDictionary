#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.tbc_ActivityReportGroupMembers

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_ActivityReportGroupMembers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_tbc_ActivityReportGroupMembers: GroupID\MSISDN](../../../../Images/pk.png)](#indexes)[![Foreign Keys FK_tbc_ActivityReportGroupMembers_tbc_ActivityReportGroups: [dbo].[tbc_ActivityReportGroups].GroupID](../../../../Images/fk.png)](#foreignkeys) | GroupID | smallint | 2 | NOT NULL |
| [![Primary Key PK_tbc_ActivityReportGroupMembers: GroupID\MSISDN](../../../../Images/pk.png)](#indexes) | MSISDN | varchar(9) | 9 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_tbc_ActivityReportGroupMembers: GroupID\MSISDN](../../../../Images/pk.png)](#indexes) | PK_tbc_ActivityReportGroupMembers | GroupID, MSISDN | YES |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_tbc_ActivityReportGroupMembers_tbc_ActivityReportGroups | GroupID->[[dbo].[tbc_ActivityReportGroups].[GroupID]](tbc_ActivityReportGroups.md) |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

