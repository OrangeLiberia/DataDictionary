#### 

[Project](../../../../index.md) > [192.168.19.44\\REPLICANT](../../../index.md) > [User databases](../../index.md) > [MaxIT](../index.md) > [Tables](Tables.md) > sugu.login_logs

# ![Tables](../../../../Images/Table32.png) [sugu].[login_logs]

---

## <a name="#description"></a>MS_Description

Stores the login and logout details of Maxit App users. Tracks user connection state, device information, and session timestamps for KPI analysis.

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Primary Key PK_login_logs: id](../../../../Images/pk.png)](#indexes) | id | bigint(19) | 19 | NOT NULL | NULL | _Unique auto-incremented identifier_ |
|  | attached | tinyint(3) | 3 | NULL allowed | 0 | _Flag indicating if the session is attached_ |
| [![Indexes IX_login_logs_created_at](../../../../Images/Index.png)](#indexes) | created_at | datetime |  | NULL allowed | current_timestamp() | _Timestamp of when the record was created_ |
| [![Indexes IX_login_logs_device_id](../../../../Images/Index.png)](#indexes) | device_id | varchar(255) | 255 | NULL allowed | NULL | _Unique identifier for the user's device_ |
|  | device_manufacturer | varchar(255) | 255 | NULL allowed | NULL | _Manufacturer of the user's device (e.g., Apple, Samsung)_ |
|  | device_model | varchar(255) | 255 | NULL allowed | NULL | _Model of the user's device (e.g., iPhone 12, Samsung Galaxy S20)_ |
|  | device_os | varchar(255) | 255 | NULL allowed | NULL | _Operating system of the user's device (e.g., Android, iOS)_ |
|  | disconnect_date | datetime |  | NULL allowed | NULL | _Timestamp of when the user logged out_ |
| [![Indexes IX_login_logs_hash](../../../../Images/Index.png)](#indexes) | hash | varchar(255) | 255 | NULL allowed | NULL | _Hash value for session validation_ |
|  | login_date | datetime |  | NULL allowed | NULL | _Timestamp of when the user logged in_ |
| [![Indexes UQ_login_logs_msisdn](../../../../Images/Index.png)](#indexes) | msisdn | varchar(255) | 255 | NOT NULL | NULL | _User's phone number (unique identifier)_ |
|  | refresh | text(65535) | 65535 | NULL allowed | NULL | _Refresh token data for the session_ |
| [![Indexes IX_login_logs_state](../../../../Images/Index.png)](#indexes) | state | varchar(255) | 255 | NULL allowed | NULL | _Indicates whether the user is CONNECTED or DISCONNECTED (login/logout status)_ |



---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_login_logs](../../../../Images/pk.png)](#indexes) | PK_login_logs | id | YES |
|  | UQ_login_logs_msisdn | msisdn | YES |
|  | IX_login_logs_created_at | created_at | NO |
|  | IX_login_logs_device_id | device_id | NO |
|  | IX_login_logs_hash | hash | NO |
|  | IX_login_logs_state | state | NO |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM
