#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Views](Views.md) > dbo.vww_AdminAuditTrail

# ![Views](../../../../Images/View32.png) [dbo].[vww_AdminAuditTrail]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| FileID | bigint | 8 |
| ID | int | 4 |
| RefDate | date | 3 |
| CurrencyType | varchar(16) | 16 |
| USER_ID | varchar(32) | 32 |
| USER_MSISDN | varchar(60) | 60 |
| LOGGED_IN | datetime | 8 |
| LOG_OUT | datetime | 8 |
| CATEGORY | varchar(32) | 32 |
| ACTION_TYPE | varchar(128) | 128 |
| ACTION_PERFORMED_ON | varchar(32) | 32 |
| BARRED_USER | varchar(32) | 32 |
| REMARKS | varchar(256) | 256 |
| CREATED_BY | varchar(20) | 20 |
| CREATED_ON | datetime | 8 |
| ATT_1_NAME | varchar(64) | 64 |
| ATT_1_VALUE | varchar(128) | 128 |
| ATT_2_NAME | varchar(64) | 64 |
| ATT_2_VALUE | varchar(128) | 128 |
| ATT_3_NAME | varchar(64) | 64 |
| ATT_3_VALUE | varchar(128) | 128 |
| SN | varchar(32) | 32 |
| TRANSACTION_ID | varchar(32) | 32 |
| Cust_ID | varchar(32) | 32 |
| STATUS_ID | varchar(2) | 2 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

