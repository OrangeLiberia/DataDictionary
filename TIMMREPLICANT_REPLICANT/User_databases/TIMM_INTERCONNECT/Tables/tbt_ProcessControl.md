#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_ProcessControl

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_ProcessControl]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_ProcessControl: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Enabled | tinyint | 1 | NULL allowed |  |
|  | ExecutionOrder | int | 4 | NULL allowed |  |
|  | ProcessID | varchar(50) | 50 | NOT NULL |  |
|  | ProcessName | varchar(max) | max | NULL allowed |  |
|  | StartStep | int | 4 | NULL allowed |  |
|  | EndStep | int | 4 | NULL allowed |  |
|  | SPName | varchar(max) | max | NULL allowed |  |
|  | Description | varchar(max) | max | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

