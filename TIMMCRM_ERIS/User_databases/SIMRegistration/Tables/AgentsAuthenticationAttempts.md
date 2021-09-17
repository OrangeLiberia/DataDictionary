#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.AgentsAuthenticationAttempts

# ![Tables](../../../../Images/Table32.png) [dbo].[AgentsAuthenticationAttempts]

---

## <a name="#description"></a>MS_Description

Log of the agent Login attemps

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default | Description |
|---|---|---|---|---|---|---|---|
|  | ID | bigint | 8 | NOT NULL | 1 - 1 |  |  |
| [![Indexes IX_Authentication](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(20) | 20 | NULL allowed |  |  | _Agent MSISDN_ |
| [![Indexes IX_Authentication](../../../../Images/Index.png)](#indexes) | IMEI | varchar(20) | 20 | NULL allowed |  |  | _Agent Device Identification_ |
| [![Indexes IX_Authentication](../../../../Images/Index.png)](#indexes) | ICCID | varchar(20) | 20 | NULL allowed |  |  | _Agent SIM_ |
|  | EncryptedParams | varchar(200) | 200 | NULL allowed |  |  |  |
|  | DateTime | datetime | 8 | NOT NULL |  | (getdate()) | _Datetime_ |
| [![Indexes IX_Authentication](../../../../Images/Index.png)](#indexes) | RetID | int | 4 | NOT NULL |  |  | _Authentication return value_ |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_Authentication | MSISDN, IMEI, ICCID, RetID |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

