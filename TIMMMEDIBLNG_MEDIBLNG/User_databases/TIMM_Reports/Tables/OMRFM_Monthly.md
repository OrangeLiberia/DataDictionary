#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.OMRFM_Monthly

# ![Tables](../../../../Images/Table32.png) [dbo].[OMRFM_Monthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 8651498 |
| Created | 10:05:56 PM Thursday, September 30, 2021 |
| Last Modified | 10:05:56 PM Thursday, September 30, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| REFMOMTH | char(7) | 7 | NULL allowed |
| MSISDN | varchar(15) | 15 | NOT NULL |
| MONTHLY_Recency_by_Creation_date | int | 4 | NULL allowed |
| MONTHLY_Recency_By_Transaction | int | 4 | NULL allowed |
| CurrencyType | varchar(16) | 16 | NOT NULL |
| MONETARY_MONTHLY | numeric(38,2) | 17 | NULL allowed |
| MONTHLY_TRANSACTIONS | int | 4 | NULL allowed |
| MONTHLY_AVERAGE_TRANSACTIONS | int | 4 | NULL allowed |
| MONTHLY_AMOUNT_SPENT | numeric(38,2) | 17 | NULL allowed |
| MONTHLY_AVERAGE_Amount | numeric(38,6) | 17 | NULL allowed |
| SEGMENT | varchar(100) | 100 | NULL allowed |
| RECOMMENDATIONS | varchar(100) | 100 | NULL allowed |
| TAG | varchar(100) | 100 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

