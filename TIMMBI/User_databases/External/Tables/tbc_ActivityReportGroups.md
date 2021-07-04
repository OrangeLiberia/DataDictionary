#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.tbc_ActivityReportGroups

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_ActivityReportGroups]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_tbc_ActivityReportGroups: GroupID](../../../../Images/pk.png)](#indexes) | GroupID | smallint | 2 | NOT NULL |
|  | GroupName | varchar(100) | 100 | NOT NULL |
|  | StartPeriod | int | 4 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_tbc_ActivityReportGroups: GroupID](../../../../Images/pk.png)](#indexes) | PK_tbc_ActivityReportGroups | GroupID | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

