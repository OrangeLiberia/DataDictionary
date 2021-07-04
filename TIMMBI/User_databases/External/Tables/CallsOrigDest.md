#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.CallsOrigDest

# ![Tables](../../../../Images/Table32.png) [dbo].[CallsOrigDest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsDestinations: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |
|  | Name | varchar(20) | 20 | NOT NULL |  |
|  | Description | varchar(250) | 250 | NULL allowed |  |
|  | NameOrig | varchar(20) | 20 | NULL allowed |  |
|  | NameDest | varchar(20) | 20 | NULL allowed |  |
|  | IsGroup | bit | 1 | NOT NULL | ((0)) |
| [![Foreign Keys FK_CallsOrigDest_IDGroup: [dbo].[CallsOrigDest].IDGroup](../../../../Images/fk.png)](#foreignkeys) | IDGroup | int | 4 | NULL allowed |  |
|  | Status | int | 4 | NOT NULL | ((1)) |
|  | LastUserID | int | 4 | NOT NULL |  |
|  | LastUpdate | datetime | 8 | NOT NULL | (getdate()) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_SubsCallsDestinations: ID](../../../../Images/pkcluster.png)](#indexes) | PK_SubsCallsDestinations | ID | YES |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_CallsOrigDest_IDGroup | IDGroup->[[dbo].[CallsOrigDest].[ID]]() |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

