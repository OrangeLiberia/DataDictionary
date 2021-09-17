#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.RTKYC

# ![Tables](../../../../Images/Table32.png) [dbo].[RTKYC]

---

## <a name="#description"></a>MS_Description

Real Time Validation Queue

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_RTKYC: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL |  | _ID_ |
| [![Indexes IX_MSISDN
IX_RTKYC_MSISDN](../../../../Images/Index.png)](#indexes)(2) | MSISDN | varchar(20) | 20 | NOT NULL |  | _Subscriber MSISDN_ |
|  | ExecState | smallint | 2 | NOT NULL |  | _SIM Registration execution status_ |
|  | ReturnID | smallint | 2 | NOT NULL |  | _SIM Registration returned id_ |
| [![Indexes IX_RTKYC_MSISDN
IX_Status](../../../../Images/Index.png)](#indexes)(2) | Status | int | 4 | NOT NULL | ((0)) | _Execution state of the validation_ |
|  | RegDate | datetime | 8 | NOT NULL | (getdate()) | _Datetime registration_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_RTKYC: ID](../../../../Images/pkcluster.png)](#indexes) | PK_RTKYC | ID | YES |
|  | IX_MSISDN | MSISDN |  |
|  | IX_RTKYC_MSISDN | MSISDN, Status |  |
|  | IX_Status | Status |  |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

