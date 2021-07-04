#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.HandSetStandard

# ![Tables](../../../../Images/Table32.png) [msc].[HandSetStandard]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetStandard: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
| [![Indexes IX_HandSetStandard](../../../../Images/Index.png)](#indexes) | Brand | varchar(256) | 256 | NOT NULL |  |
| [![Indexes IX_HandSetStandard](../../../../Images/Index.png)](#indexes) | Model | varchar(512) | 512 | NOT NULL |  |
|  | PictureName | varchar(256) | 256 | NULL allowed |  |
|  | Picture | image | max | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetStandard: ID](../../../../Images/pkcluster.png)](#indexes) | PK_HandSetStandard | ID | YES |  |
|  | IX_HandSetStandard | Brand, Model |  | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[HandSetInfo]](HandSetInfo.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

