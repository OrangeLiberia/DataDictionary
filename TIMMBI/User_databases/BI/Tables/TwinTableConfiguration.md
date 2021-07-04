#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.TwinTableConfiguration

# ![Tables](../../../../Images/Table32.png) [fwk].[TwinTableConfiguration]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TwinTableConfiguration: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Check Constraints CK_TwinTableConfiguration_Unit : ([Unit]='Week' OR [Unit]='Year' OR [Unit]='Month' OR [Unit]='Day')](../../../../Images/c-constraint.png)](#checkconstraints) | Unit | varchar(20) | 20 | NOT NULL |  |  |
|  | Value | int | 4 | NOT NULL |  |  |
|  | TableName | varchar(200) | 200 | NOT NULL |  |  |
|  | ViewPrefix | varchar(20) | 20 | NOT NULL |  |  |
|  | ReferenceDate | datetime | 8 | NOT NULL |  |  |
|  | Status | int | 4 | NOT NULL |  | ((1)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TwinTableConfiguration: ID](../../../../Images/pkcluster.png)](#indexes) | PK_TwinTableConfiguration | ID | YES | FWK |


---

## <a name="#checkconstraints"></a>Check Constraints

| Name | On Column | Constraint |
|---|---|---|
| CK_TwinTableConfiguration_Unit | Unit | ([Unit]='Week' OR [Unit]='Year' OR [Unit]='Month' OR [Unit]='Day') |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spt_TwinTablesBackup]](../Programmability/Stored_Procedures/spt_TwinTablesBackup.md)
* [[fwk].[spt_TwinTablesChangeView]](../Programmability/Stored_Procedures/spt_TwinTablesChangeView.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

