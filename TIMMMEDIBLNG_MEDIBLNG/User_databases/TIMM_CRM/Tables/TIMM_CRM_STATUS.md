#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.TIMM_CRM_STATUS

# ![Tables](../../../../Images/Table32.png) [dbo].[TIMM_CRM_STATUS]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Persisted | Computed | Max Length (Bytes) | Nullability |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TIMM_INV_PARAMETROS: TableName\ColumnName\Value](../../../../Images/pkcluster.png)](#indexes) | TableName | varchar(200) |  |  | 200 | NOT NULL |
| [![Cluster Primary Key PK_TIMM_INV_PARAMETROS: TableName\ColumnName\Value](../../../../Images/pkcluster.png)](#indexes) | ColumnName | varchar(200) |  |  | 200 | NOT NULL |
|  | Description | varchar(200) |  |  | 200 | NOT NULL |
|  | KeyCode | varchar(200) |  |  | 200 | NULL allowed |
| [![Cluster Primary Key PK_TIMM_INV_PARAMETROS: TableName\ColumnName\Value](../../../../Images/pkcluster.png)](#indexes) | Value | varchar(200) |  |  | 200 | NOT NULL |
|  | ValueNumberic | int | YES | YES | 4 | NULL allowed |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| ValueNumberic | (CONVERT([int],case  when isnumeric([Value])=(1) then [Value] end,(0))) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

