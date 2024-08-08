#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.OmdailyRFMFromLedger

# ![Tables](../../../../Images/Table32.png) [dbo].[OmdailyRFMFromLedger]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 36252441 |
| Created | 3:57:33 PM Thursday, September 30, 2021 |
| Last Modified | 3:57:33 PM Thursday, September 30, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| Previous_TX_Date | date | 3 | NULL allowed |
| DAYS_BEWEEN_DATE_AND_ | int | 4 | NULL allowed |
| Refdate | date | 3 | NOT NULL |
| CREATION_DATE | datetime | 8 | NULL allowed |
| SERVICE_TYPE | varchar(10) | 10 | NOT NULL |
| DESIGNATION | varchar(30) | 30 | NULL allowed |
| DOMAIN_CODE | varchar(10) | 10 | NULL allowed |
| TAG | varchar(100) | 100 | NULL allowed |
| TRANSACTION_TYPE | varchar(8) | 8 | NOT NULL |
| FRIST_OF_MONTH | date | 3 | NULL allowed |
| LAST_OF_MONTH | date | 3 | NULL allowed |
| ACCOUNT_LEVEL | varchar(10) | 10 | NULL allowed |
| GRADE | varchar(40) | 40 | NULL allowed |
| STATE | varchar(30) | 30 | NULL allowed |
| Weekly_TOTAL_AMOUNT_SPEND_PER_SERVICE | numeric(38,2) | 17 | NULL allowed |
| Weekly_TRANSACTIONS_PER_SERVICE | int | 4 | NULL allowed |
| TRANSACTION_TAG | varchar(50) | 50 | NOT NULL |
| CurrencyType | varchar(16) | 16 | NOT NULL |
| MSISDN | varchar(15) | 15 | NOT NULL |
| NAME | varchar(80) | 80 | NULL allowed |
| Commisison_Earn | numeric(38,2) | 17 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

