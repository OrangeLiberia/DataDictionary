#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.ConfigurationParameters

# ![Tables](../../../../Images/Table32.png) [fwk].[ConfigurationParameters]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
|  | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Cluster Primary Key PK_ConfigurationParameters: ParameterName](../../../../Images/pkcluster.png)](#indexes) | ParameterName | varchar(50) | 50 | NOT NULL |  |  |
|  | Value | varchar(max) | max | NULL allowed |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  | (getdate()) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ConfigurationParameters: ParameterName](../../../../Images/pkcluster.png)](#indexes) | PK_ConfigurationParameters | ParameterName | YES | FWK |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[fwk].[fnt_GetConfigurationParameter]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetConfigurationParameter.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

