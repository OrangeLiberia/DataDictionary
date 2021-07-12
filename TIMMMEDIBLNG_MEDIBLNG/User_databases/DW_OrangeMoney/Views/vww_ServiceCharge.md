#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Views](Views.md) > dbo.vww_ServiceCharge

# ![Views](../../../../Images/View32.png) [dbo].[vww_ServiceCharge]

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
| SERVICE_CHARGE_ID | numeric(10,0) | 9 |
| NETWORK_NAME | varchar(2) | 2 |
| PROFILE_NAME | varchar(40) | 40 |
| SHORT_CODE | varchar(20) | 20 |
| SERVICE_TYPE | varchar(10) | 10 |
| PAYER_GRADE_CODE | varchar(10) | 10 |
| PAYEE_GRADE_CODE | varchar(10) | 10 |
| SERVICE_CHARGE_VERSION | numeric(10,0) | 9 |
| START_DATETIME | datetime | 8 |
| MIN_TRANSFER_VALUE | numeric(19,2) | 9 |
| MAX_TRANSFER_VALUE | numeric(19,2) | 9 |
| MULTIPLE_OF | numeric(19,2) | 9 |
| MIN_FIXED_SERVICE_CHARGE | numeric(19,2) | 9 |
| MAX_FIXED_SERVICE_CHARGE | numeric(19,2) | 9 |
| MIN_PCT_SERVICE_CHARGE | numeric(19,2) | 9 |
| MAX_PCT_SERVICE_CHARGE | numeric(19,2) | 9 |
| START_RANGE | numeric(19,2) | 9 |
| END_RANGE | numeric(19,2) | 9 |
| FIXED_SERVICE_CHARGE | numeric(19,2) | 9 |
| PCT_SERVICE_CHARGE | numeric(19,2) | 9 |
| CREATED_BY | varchar(30) | 30 |
| CREATED_ON | datetime | 8 |
| MODIFIED_BY | varchar(30) | 30 |
| MODIFIED_ON | datetime | 8 |
| PAYER_PAYMENT_TYPE_ID | numeric(2,0) | 5 |
| PAYEE_PAYMENT_TYPE_ID | numeric(2,0) | 5 |
| IS_FINANCIAL | varchar(1) | 1 |
| SERVICE_CHARGE_NONFIN | numeric(22,0) | 13 |
| STATUS_ID | varchar(2) | 2 |
| PAYER_CATEGORY_CODE | varchar(10) | 10 |
| PAYER_TYPE | varchar(10) | 10 |
| CREDIT_ENTITY | varchar(20) | 20 |
| DEBIT_ENTITY | varchar(20) | 20 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

