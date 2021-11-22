#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Views](Views.md) > dbo.vww_APGL

# ![Views](../../../../Images/View32.png) [dbo].[vww_APGL]

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
| SENDER_MSISDN | varchar(60) | 60 |
| RECEIVER_MSISDN | varchar(60) | 60 |
| SENDER_USER_ID | varchar(20) | 20 |
| RECEIVER_USER_ID | varchar(20) | 20 |
| SERVICE_TYPE | varchar(10) | 10 |
| TRANSFER_SUBTYPE | varchar(10) | 10 |
| SENDER_COUNTRY_CODE | varchar(2) | 2 |
| RECEIVER_COUNTRY_CODE | varchar(2) | 2 |
| TRANSACTION_STATUS | varchar(3) | 3 |
| SENDER_PRE_BALANCE | numeric(17,2) | 9 |
| SENDER_POST_BALANCE | numeric(17,2) | 9 |
| RECEIVER_PRE_BALANCE | numeric(17,2) | 9 |
| RECEIVER_POST_BALANCE | numeric(17,2) | 9 |
| REFERENCE_NUMBER | varchar(255) | 255 |
| REMARKS | varchar(150) | 150 |
| TRANSACTION_ID | varchar(20) | 20 |
| TRANSACTION_DATE_TIME | datetime | 8 |
| SENDER_CATEGORY_CODE | varchar(20) | 20 |
| RECEIVER_CATEGORY_CODE | varchar(20) | 20 |
| SENDER_DOMAIN_CODE | varchar(10) | 10 |
| RECEIVER_DOMAIN_CODE | varchar(10) | 10 |
| SENDER_DESIGNATION | varchar(30) | 30 |
| RECEIVER_DESIGNATION | varchar(30) | 30 |
| SENDER_STATE | varchar(60) | 60 |
| RECEIVER_STATE | varchar(60) | 60 |
| TRANSACTION_AMOUNT | numeric(17,2) | 9 |
| COMMISSION_GROSSISTE | numeric(17,2) | 9 |
| COMMISSION_AGENT | numeric(17,2) | 9 |
| COMMISSION_OCA | numeric(17,2) | 9 |
| COMMISSION_AUTRE | numeric(17,2) | 9 |
| SERVICE_CHARGE_AMOUNT | numeric(17,2) | 9 |
| TRANSACTION_TAG | varchar(50) | 50 |
| IS_FINANCIAL | varchar(1) | 1 |
| ZEBRA | varchar(10) | 10 |
| ROLLBACKED | varchar(1) | 1 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

