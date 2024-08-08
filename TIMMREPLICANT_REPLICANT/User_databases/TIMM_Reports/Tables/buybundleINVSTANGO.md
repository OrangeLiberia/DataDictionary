#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.buybundleINVSTANGO

# ![Tables](../../../../Images/Table32.png) [dbo].[buybundleINVSTANGO]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 24134205 |
| Created | 1:40:56 PM Thursday, September 30, 2021 |
| Last Modified | 1:40:56 PM Thursday, September 30, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__buybundl__3214EC2763D85B48: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | sender_siteID | varchar(60) | 60 | NULL allowed |  |
|  | TRANSFER_DATETIME | datetime | 8 | NULL allowed |  |
|  | RECEIVER_SITEID | varchar(60) | 60 | NULL allowed |  |
|  | transfer_id | varchar(70) | 70 | NULL allowed |  |
|  | RefDate | date | 3 | NULL allowed |  |
|  | SENDER_MSISDN | varchar(70) | 70 | NULL allowed |  |
|  | RECEIVER_MSISDN | varchar(70) | 70 | NULL allowed |  |
|  | SERVICE_TYPE | varchar(70) | 70 | NULL allowed |  |
|  | TRANSFER_STATUS | varchar(70) | 70 | NULL allowed |  |
|  | BUNDLE_NAME | varchar(70) | 70 | NULL allowed |  |
|  | currencytype | varchar(70) | 70 | NULL allowed |  |
|  | TRANSACTION_AMOUNT | numeric(19,2) | 9 | NULL allowed |  |
|  | Parent_Name | varchar(70) | 70 | NULL allowed |  |
|  | PayerMSISDN | varchar(70) | 70 | NULL allowed |  |
|  | RecipientMSISDN | varchar(70) | 70 | NULL allowed |  |
|  | OMTransID | varchar(70) | 70 | NULL allowed |  |
|  | TypeActivation | varchar(70) | 70 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

