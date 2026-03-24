#### 

[Project](../../../../index.md) > [192.168.19.44\\REPLICANT](../../../index.md) > [User databases](../../index.md) > [MaxIT](../index.md) > [Tables](Tables.md) > sugu.service_usage_logs

# ![Tables](../../../../Images/Table32.png) [sugu].[service_usage_logs]

---

## <a name="#description"></a>MS_Description

Stores details of user interactions with various services in the Maxit App. Captures transaction information, device details, service types, and request metadata for KPI analysis and service engagement tracking.

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Primary Key PK_service_usage_logs: id](../../../../Images/pk.png)](#indexes) | id | bigint(19) | 19 | NOT NULL | NULL | _Unique auto-incremented identifier_ |
|  | amount | varchar(255) | 255 | NULL allowed | NULL | _Amount paid by the user in case of a transaction or service usage_ |
| [![Indexes IX_service_usage_logs_app_version](../../../../Images/Index.png)](#indexes) | app_version | varchar(255) | 255 | NULL allowed | NULL | _Version of the Maxit app being used during the transaction_ |
| [![Indexes IX_service_usage_logs_date_action](../../../../Images/Index.png)](#indexes) | date_action | datetime |  | NULL allowed | NULL | _Timestamp of the action as recorded by the application_ |
| [![Indexes IX_service_usage_logs_date_action_systeme](../../../../Images/Index.png)](#indexes) | date_action_systeme | datetime |  | NULL allowed | NULL | _Timestamp of the action as recorded by the system_ |
|  | extra_data | varchar(255) | 255 | NULL allowed | NULL | _Additional information or data associated with the request_ |
|  | fee | varchar(255) | 255 | NULL allowed | NULL | _Fee applied to the transaction or service usage, if applicable_ |
|  | ip_address | varchar(255) | 255 | NULL allowed | NULL | _IP address of the user (user agent IP)_ |
|  | localisation | varchar(255) | 255 | NULL allowed | NULL | _Geolocation coordinates of the user during the transaction_ |
|  | localisation_address | varchar(255) | 255 | NULL allowed | NULL | _Human-readable address of the user's location during the transaction_ |
| [![Indexes IX_service_usage_logs_msisdn](../../../../Images/Index.png)](#indexes) | msisdn | varchar(255) | 255 | NULL allowed | NULL | _User's phone number_ |
|  | request | varchar(255) | 255 | NULL allowed | NULL | _Raw request data associated with the service call_ |
| [![Indexes IX_service_usage_logs_service](../../../../Images/Index.png)](#indexes) | service | varchar(255) | 255 | NULL allowed | NULL | _Service the user interacted with (e.g., B2W, BUY_CREDIT, OMY_P2P_TRANSFER, TNO, CASHIN, CASHOUT, etc.)_ |
|  | source | varchar(255) | 255 | NULL allowed | NULL | _User agent indicating the source of the request (usually mobile app)_ |
| [![Indexes IX_service_usage_logs_status](../../../../Images/Index.png)](#indexes) | status | varchar(255) | 255 | NULL allowed | NULL | _Status of the request (e.g., cODE:2000;message:success)_ |
|  | terminal_manufacturer | varchar(255) | 255 | NULL allowed | NULL | _Manufacturer of the terminal (e.g., Apple, Samsung)_ |
|  | terminal_model | varchar(255) | 255 | NULL allowed | NULL | _Model of the terminal used during the transaction_ |
| [![Indexes IX_service_usage_logs_terminal_os](../../../../Images/Index.png)](#indexes) | terminal_os | varchar(255) | 255 | NULL allowed | NULL | _Operating system of the terminal (e.g., Android, iOS)_ |
|  | terminal_uiid | varchar(255) | 255 | NULL allowed | NULL | _Unique identifier of the terminal device_ |
|  | terminal_version | varchar(255) | 255 | NULL allowed | NULL | _Version of the terminal's operating system_ |
|  | txn_id | varchar(255) | 255 | NULL allowed | NULL | _Unique transaction ID generated for each transaction_ |
|  | utilisateur | varchar(255) | 255 | NULL allowed | NULL | _User identifier within the system_ |
| [![Indexes IX_service_usage_logs_wallet](../../../../Images/Index.png)](#indexes) | wallet | varchar(255) | 255 | NULL allowed | NULL | _Wallet identifier used for the transaction_ |
| [![Indexes IX_service_usage_logs_ref](../../../../Images/Index.png)](#indexes) | ref | varchar(255) | 255 | NULL allowed | NULL | _Reference identifier for the transaction_ |
| [![Indexes IX_service_usage_logs_currency](../../../../Images/Index.png)](#indexes) | currency | varchar(255) | 255 | NULL allowed | NULL | _Currency used for the transaction (LRD or USD)_ |



---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_service_usage_logs](../../../../Images/pk.png)](#indexes) | PK_service_usage_logs | id | YES |
|  | IX_service_usage_logs_app_version | app_version | NO |
|  | IX_service_usage_logs_date_action | date_action | NO |
|  | IX_service_usage_logs_date_action_systeme | date_action_systeme | NO |
|  | IX_service_usage_logs_msisdn | msisdn | NO |
|  | IX_service_usage_logs_service | service | NO |
|  | IX_service_usage_logs_status | status | NO |
|  | IX_service_usage_logs_terminal_os | terminal_os | NO |
|  | IX_service_usage_logs_wallet | wallet | NO |
|  | IX_service_usage_logs_ref | ref | NO |
|  | IX_service_usage_logs_currency | currency | NO |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM
