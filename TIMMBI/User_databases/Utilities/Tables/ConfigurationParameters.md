#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [Utilities](../index.md) > [Tables](Tables.md) > dbo.ConfigurationParameters

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

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

