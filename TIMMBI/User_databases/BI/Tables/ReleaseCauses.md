#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.ReleaseCauses

# ![Tables](../../../../Images/Table32.png) [msc].[ReleaseCauses]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ReleaseCauses: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | Description | varchar(100) | 100 | NOT NULL |
|  | DescWithIndex | varchar(100) | 100 | NOT NULL |
|  | CriticLevel | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ReleaseCauses: ID](../../../../Images/pkcluster.png)](#indexes) | PK_ReleaseCauses | ID | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[spc_UpdateListTables]](../Programmability/Stored_Procedures/spc_UpdateListTables.md)
* [[msc].[spt_GetCellReleaseCausesDaily]](../Programmability/Stored_Procedures/spt_GetCellReleaseCausesDaily.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

