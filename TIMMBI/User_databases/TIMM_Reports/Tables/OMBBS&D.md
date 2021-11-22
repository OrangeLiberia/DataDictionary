#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.OMBBS&D

# ![Tables](../../../../Images/Table32.png) [dbo].[OMBBS&D]

---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__OMBBS&D__3214EC27E6004772: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes IX_Sender](../../../../Images/Index.png)](#indexes) | SENDER_SITE_ID | varchar(10) | 10 | NULL allowed |  |
| [![Indexes IX_Receiver
IX_Sender](../../../../Images/Index.png)](#indexes)(2) | TRANSFER_DATETIME | datetime | 8 | NOT NULL |  |
| [![Indexes IX_Receiver](../../../../Images/Index.png)](#indexes) | RECEIVER_SITE_ID | varchar(10) | 10 | NULL allowed |  |
|  | TRANSFER_ID | varchar(20) | 20 | NOT NULL |  |
|  | RefDate | date | 3 | NOT NULL |  |
| [![Indexes IX_Sender](../../../../Images/Index.png)](#indexes) | SENDER_MSISDN | varchar(15) | 15 | NOT NULL |  |
|  | BUNDLE_WALLET | varchar(15) | 15 | NOT NULL |  |
|  | SERVICE_TYPE | varchar(10) | 10 | NOT NULL |  |
|  | TRANSFER_STATUS | varchar(3) | 3 | NOT NULL |  |
| [![Indexes IX_Receiver
IX_Sender](../../../../Images/Index.png)](#indexes)(2) | BUNDLE_NAME | varchar(128) | 128 | NULL allowed |  |
| [![Indexes IX_Receiver
IX_Sender](../../../../Images/Index.png)](#indexes)(2) | CURRENCYTYPE | varchar(16) | 16 | NOT NULL |  |
|  | TRANSACTION_AMOUNT | numeric(17,2) | 9 | NOT NULL |  |
|  | PARENT_MSISDN | varchar(200) | 200 | NULL allowed |  |
|  | SENDER_MSISDN_PAYER | varchar(32) | 32 | NULL allowed |  |
| [![Indexes IX_Receiver](../../../../Images/Index.png)](#indexes) | RECEIVER_MSISDN | varchar(32) | 32 | NULL allowed |  |
| [![Indexes IX_Receiver
IX_Sender](../../../../Images/Index.png)](#indexes)(2) | TypeActivation | varchar(6) | 6 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__OMBBS&D__3214EC27E6004772: ID](../../../../Images/pkcluster.png)](#indexes) | PK__OMBBS&D__3214EC27E6004772 | ID | YES |
|  | IX_Receiver | RECEIVER_SITE_ID, TRANSFER_DATETIME, RECEIVER_MSISDN, BUNDLE_NAME, CURRENCYTYPE, TypeActivation |  |
|  | IX_Sender | SENDER_SITE_ID, TRANSFER_DATETIME, SENDER_MSISDN, BUNDLE_NAME, CURRENCYTYPE, TypeActivation |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

