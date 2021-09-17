#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.RTKYC_Archive

# ![Tables](../../../../Images/Table32.png) [dbo].[RTKYC_Archive]

---

## <a name="#description"></a>MS_Description

Real Time Validation Queue Archive

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_RTKYC_Archive: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL |  | _ID_ |
|  | MSISDN | varchar(20) | 20 | NOT NULL |  | _Subscriber MSISDN_ |
|  | UserID | int | 4 | NOT NULL |  | _TIMM user id_ |
|  | IID | bigint | 8 | NULL allowed |  | _Interaction ID_ |
|  | MID | bigint | 8 | NULL allowed |  | _Master Interaction ID_ |
|  | ActionDT | datetime | 8 | NOT NULL | ((0)) | _Datetime of entry of registration_ |
|  | Status | int | 4 | NOT NULL |  | _Validation status_ |
|  | ValidationSeconds | int | 4 | NULL allowed |  | _Time in seconds that the validation took_ |
|  | ValidationTime | datetime | 8 | NULL allowed |  | _Datetime of the validation_ |
|  | ValidationStatus | int | 4 | NULL allowed |  | _Validation _ |
|  | ValidationDescription | varchar(256) | 256 | NULL allowed |  | _Validation description_ |
|  | Message | varchar(256) | 256 | NULL allowed |  | _System message_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_RTKYC_Archive: ID](../../../../Images/pkcluster.png)](#indexes) | PK_RTKYC_Archive | ID | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

