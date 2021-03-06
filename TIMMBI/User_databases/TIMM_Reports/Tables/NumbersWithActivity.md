#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.NumbersWithActivity

# ![Tables](../../../../Images/Table32.png) [dbo].[NumbersWithActivity]

---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Indexes IX_#NumbersWithActivity](../../../../Images/Index.png)](#indexes) | RefDate | date | 3 | NULL allowed |  |
| [![Indexes IX_#NumbersWithActivity](../../../../Images/Index.png)](#indexes) | MSISDN8 | varchar(64) | 64 | NULL allowed |  |
| [![Indexes IX_#NumbersWithActivity](../../../../Images/Index.png)](#indexes) | MSISDN9 | varchar(64) | 64 | NULL allowed |  |
|  | ServicoID | numeric(18,0) | 9 | NULL allowed |  |
|  | ContaID | numeric(18,0) | 9 | NULL allowed |  |
|  | ClienteID | numeric(18,0) | 9 | NULL allowed |  |
|  | ServicoStatus | int | 4 | NULL allowed | ((0)) |
|  | ControlStatus | int | 4 | NULL allowed | ((0)) |
|  | BILastActivity | datetime | 8 | NULL allowed |  |
|  | IDRangeMonth6 | int | 4 | NULL allowed |  |
|  | IDRangeMonth5 | int | 4 | NULL allowed |  |
|  | IDRangeMonth4 | int | 4 | NULL allowed |  |
|  | IDRangeMonth3 | int | 4 | NULL allowed |  |
|  | IDRangeMonth2 | int | 4 | NULL allowed |  |
|  | IDRangeMonth1 | int | 4 | NULL allowed |  |
|  | IDRangeMonth0 | int | 4 | NULL allowed |  |
|  | RateBillMonth6 | numeric(18,5) | 9 | NULL allowed |  |
|  | RateBillMonth5 | numeric(18,5) | 9 | NULL allowed |  |
|  | RateBillMonth4 | numeric(18,5) | 9 | NULL allowed |  |
|  | RateBillMonth3 | numeric(18,5) | 9 | NULL allowed |  |
|  | RateBillMonth2 | numeric(18,5) | 9 | NULL allowed |  |
|  | RateBillMonth1 | numeric(18,5) | 9 | NULL allowed |  |
|  | RateBillMonth0 | numeric(18,5) | 9 | NULL allowed |  |
|  | TotalRevenue | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth6 | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth5 | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth4 | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth3 | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth2 | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth1 | numeric(18,5) | 9 | NULL allowed |  |
|  | RevenueMonth0 | numeric(18,5) | 9 | NULL allowed |  |
|  | RegistrationStatus | int | 4 | NULL allowed | ((0)) |
|  | LastRegistrationDate | datetime | 8 | NULL allowed |  |
|  | NumOfRegistrations | int | 4 | NULL allowed | ((0)) |
|  | TypeOfSubs | int | 4 | NULL allowed | ((0)) |
|  | NetworkAccess | int | 4 | NULL allowed | ((0)) |
|  | ValidationXML | varchar(max) | max | NULL allowed |  |
|  | SimTracking | date | 3 | NULL allowed |  |
|  | TypeOfData | int | 4 | NULL allowed |  |
|  | TipoDoc | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_#NumbersWithActivity | MSISDN9, MSISDN8, RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

