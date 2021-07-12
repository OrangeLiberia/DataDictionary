#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.AuditPinNeverModified_ChannelUser

# ![Tables](../../../../Images/Table32.png) [dbo].[AuditPinNeverModified_ChannelUser]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_AuditPinNeverModified_ChannelUserv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_AuditPinNeverModified_ChannelUserv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_AuditPinNeverModified_ChannelUserv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
|  | CurrencyType | varchar(16) | 16 | NULL allowed |
|  | USER_ID | varchar(20) | 20 | NOT NULL |
|  | MSISDN | varchar(20) | 20 | NOT NULL |
|  | USER_FIRST_NAME | varchar(80) | 80 | NULL allowed |
|  | USER_LAST_NAME | varchar(80) | 80 | NULL allowed |
|  | CATEGORY_CODE | varchar(10) | 10 | NOT NULL |
|  | Created_on | datetime | 8 | NULL allowed |
|  | Type_User | varchar(20) | 20 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_AuditPinNeverModified_ChannelUserv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_AuditPinNeverModified_ChannelUserv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

