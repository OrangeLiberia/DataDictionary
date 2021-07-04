#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.Status

# ![Tables](../../../../Images/Table32.png) [fwk].[Status]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Status: ID\TableName](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_Status: ID\TableName](../../../../Images/pkcluster.png)](#indexes) | TableName | varchar(200) | 200 | NOT NULL |  |
|  | Description | varchar(250) | 250 | NULL allowed |  |
|  | LastUserID | int | 4 | NOT NULL |  |
|  | LastUpdate | datetime | 8 | NOT NULL | (getdate()) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Status: ID\TableName](../../../../Images/pkcluster.png)](#indexes) | PK_Status | ID, TableName | YES | FWK |


---

## <a name="#uses"></a>Uses

* [fwk]


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

