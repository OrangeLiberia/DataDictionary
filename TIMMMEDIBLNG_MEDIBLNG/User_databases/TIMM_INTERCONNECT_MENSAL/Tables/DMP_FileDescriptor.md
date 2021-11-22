#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.DMP_FileDescriptor

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_FileDescriptor]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_FileDescriptor: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | FileID | bigint | 8 | NOT NULL |  |  |
|  | CommitCharge | int | 4 | NULL allowed |  |  |
|  | FK_Central_ID | int | 4 | NOT NULL |  |  |
|  | QOS_Processing | bit | 1 | NOT NULL |  | ((0)) |
|  | ICON_Processing | int | 4 | NOT NULL |  | ((0)) |
|  | CDR_Deleted | int | 4 | NOT NULL |  | ((0)) |
|  | FirstCDRTime | datetime | 8 | NULL allowed |  |  |
|  | LastCDRTime | datetime | 8 | NULL allowed |  |  |
|  | DBName | varchar(50) | 50 | NOT NULL |  | (db_name()) |
|  | ICON_Reprocessing | int | 4 | NULL allowed |  | ((100)) |
|  | ProcessError | int | 4 | NULL allowed |  | ((0)) |
|  | ReprocessError | int | 4 | NULL allowed |  | ((0)) |
|  | SMS_Processing | int | 4 | NOT NULL |  | ((0)) |
|  | SMS_Reprocessing | int | 4 | NULL allowed |  |  |
|  | SMS_ProcessError | int | 4 | NULL allowed |  |  |
|  | SMS_ReprocessError | int | 4 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

