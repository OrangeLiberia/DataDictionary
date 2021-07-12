#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Views](Views.md) > dbo.vww_AuditTrail

# ![Views](../../../../Images/View32.png) [dbo].[vww_AuditTrail]

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
| TRANSACTION_ID | varchar(32) | 32 |
| Cust_ID | varchar(32) | 32 |
| USER_ID | varchar(32) | 32 |
| User_Access_ID | varchar(60) | 60 |
| SERVICE_TYPE | varchar(10) | 10 |
| TRANSFER_SUBTYPE | varchar(10) | 10 |
| Account1 | varchar(32) | 32 |
| Account2 | varchar(32) | 32 |
| Transaction_Status | varchar(3) | 3 |
| Transaction_Date | datetime | 8 |
| Transaction_On | datetime | 8 |
| ERROR_CODE | varchar(20) | 20 |
| Comments | varchar(256) | 256 |
| ATT_1_NAME | varchar(64) | 64 |
| ATT_1_VALUE | varchar(128) | 128 |
| ATT_2_NAME | varchar(64) | 64 |
| ATT_2_VALUE | varchar(128) | 128 |
| ATT_3_NAME | varchar(64) | 64 |
| ATT_3_VALUE | varchar(128) | 128 |
| Sender_MFS_Provider | varchar(64) | 64 |
| Sender_Payment_Instrument | varchar(64) | 64 |
| Sender_Wallet_Type | varchar(64) | 64 |
| Sender_Linked_Bank | varchar(64) | 64 |
| Receiver_MFS_Provider | varchar(64) | 64 |
| Receiver_Payment_Instrument | varchar(64) | 64 |
| Receiver_Wallet_Type | varchar(64) | 64 |
| Receiver_Linked_Bank | varchar(256) | 256 |
| Transaction_Mode | varchar(512) | 512 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

