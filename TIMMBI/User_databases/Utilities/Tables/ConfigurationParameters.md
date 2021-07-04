#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [Utilities](../index.md) > [Tables](Tables.md) > dbo.ConfigurationParameters

# ![Tables](../../../../Images/Table32.png) [dbo].[ConfigurationParameters]

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

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ConfigurationParameters: ParameterName](../../../../Images/pkcluster.png)](#indexes) | PK_ConfigurationParameters | ParameterName | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

