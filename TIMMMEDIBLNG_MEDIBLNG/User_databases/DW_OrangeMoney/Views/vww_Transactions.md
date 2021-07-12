#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Views](Views.md) > dbo.vww_Transactions

# ![Views](../../../../Images/View32.png) [dbo].[vww_Transactions]

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
| SENDER_MSISDN | varchar(15) | 15 |
| RECEIVER_MSISDN | varchar(15) | 15 |
| RECEIVER_USER_ID | varchar(20) | 20 |
| SENDER_USER_ID | varchar(20) | 20 |
| TRANSACTION_AMOUNT | numeric(17,2) | 9 |
| COMMISSIONS_PAID | numeric(17,2) | 9 |
| COMMISSIONS_RECEIVED | numeric(17,2) | 9 |
| COMMISSIONS_OTHERS | numeric(17,2) | 9 |
| SERVICE_CHARGE_RECEIVED | numeric(17,2) | 9 |
| SERVICE_CHARGE_PAID | numeric(17,2) | 9 |
| TAXES | numeric(17,2) | 9 |
| SERVICE_TYPE | varchar(10) | 10 |
| TRANSFER_STATUS | varchar(3) | 3 |
| SENDER_PRE_BAL | numeric(17,2) | 9 |
| SENDER_POST_BAL | numeric(17,2) | 9 |
| RECEIVER_PRE_BAL | numeric(17,2) | 9 |
| RECEIVER_POST_BAL | numeric(17,2) | 9 |
| SENDER_ACC_STATUS | varchar(2) | 2 |
| RECEIVER_ACC_STATUS | varchar(2) | 2 |
| ERROR_CODE | varchar(20) | 20 |
| ERROR_DESC | varchar(350) | 350 |
| REFERENCE_NUMBER | varchar(100) | 100 |
| CREATED_ON | datetime | 8 |
| CREATED_BY | varchar(20) | 20 |
| MODIFIED_ON | datetime | 8 |
| MODIFIED_BY | varchar(20) | 20 |
| APP_1_DATE | datetime | 8 |
| APP_2_DATE | datetime | 8 |
| TRANSFER_ID | varchar(20) | 20 |
| TRANSFER_DATETIME | datetime | 8 |
| SENDER_CATEGORY_CODE | varchar(10) | 10 |
| SENDER_DOMAIN_CODE | varchar(10) | 10 |
| SENDER_GRADE_NAME | varchar(40) | 40 |
| SENDER_GROUP_ROLE | varchar(35) | 35 |
| SENDER_DESIGNATION | varchar(30) | 30 |
| SENDER_STATE | varchar(30) | 30 |
| RECEIVER_CATEGORY_CODE | varchar(10) | 10 |
| RECEIVER_DOMAIN_CODE | varchar(10) | 10 |
| RECEIVER_GRADE_NAME | varchar(40) | 40 |
| RECEIVER_GROUP_ROLE | varchar(35) | 35 |
| RECEIVER_DESIGNATION | varchar(30) | 30 |
| RECEIVER_STATE | varchar(30) | 30 |
| SENDER_CITY | varchar(30) | 30 |
| RECEIVER_CITY | varchar(30) | 30 |
| APP_1_BY | varchar(30) | 30 |
| APP_2_BY | varchar(30) | 30 |
| REQUEST_SOURCE | varchar(10) | 10 |
| GATEWAY_TYPE | varchar(10) | 10 |
| TRANSFER_SUBTYPE | varchar(10) | 10 |
| PAYMENT_TYPE | varchar(255) | 255 |
| PAYMENT_NUMBER | varchar(255) | 255 |
| PAYMENT_DATE | datetime | 8 |
| REMARKS | varchar(100) | 100 |
| ACTION_TYPE | varchar(20) | 20 |
| TRANSACTION_TAG | varchar(50) | 50 |
| RECONCILIATION_BY | varchar(20) | 20 |
| RECONCILIATION_FOR | varchar(50) | 50 |
| EXT_TXN_NUMBER | varchar(50) | 50 |
| ORIGINAL_REF_NUMBER | varchar(100) | 100 |
| ZEBRA_AMBIGUOUS | varchar(10) | 10 |
| ATTEMPT_STATUS | varchar(20) | 20 |
| OTHER_MSISDN | varchar(255) | 255 |
| SENDER_WALLET_NUMBER | varchar(25) | 25 |
| RECEIVER_WALLET_NUMBER | varchar(25) | 25 |
| SENDER_USER_NAME | varchar(80) | 80 |
| RECEIVER_USER_NAME | varchar(80) | 80 |
| TNO_MSIDN | varchar(15) | 15 |
| TNO_ID | varchar(30) | 30 |
| UNREG_FIRST_NAME | varchar(80) | 80 |
| UNREG_LAST_NAME | varchar(80) | 80 |
| UNREG_DOB | datetime | 8 |
| UNREG_ID_NUMBER | varchar(15) | 15 |
| BULK_PAYOUT_BATCHID | varchar(255) | 255 |
| IS_FINANCIAL | varchar(1) | 1 |
| TRANSFER_DONE | varchar(1) | 1 |
| INITIATOR_MSISDN | varchar(16) | 16 |
| VALIDATOR_MSISDN | varchar(16) | 16 |
| INITIATOR_COMMENTS | varchar(96) | 96 |
| VALIDATOR_COMMENTS | varchar(96) | 96 |
| SENDER_WALLET_NAME | varchar(64) | 64 |
| RECEIVER_WALLET_NAME | varchar(64) | 64 |
| SENDER_USER_TYPE | varchar(64) | 64 |
| RECEIVER_USER_TYPE | varchar(64) | 64 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

