#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgRoamingRating_TaxUpdate_20170531

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgRoamingRating_TaxUpdate_20170531]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| ID | bigint | 8 | NOT NULL | 1 - 1 |
| IDAgreement | bigint | 8 | NOT NULL |  |
| ZoneID | bigint | 8 | NOT NULL |  |
| ScheduleID | int | 4 | NOT NULL |  |
| Daytype | varchar(10) | 10 | NOT NULL |  |
| InitialInterval | int | 4 | NULL allowed |  |
| InitialRate | decimal(18,10) | 9 | NULL allowed |  |
| BillingInterval | int | 4 | NULL allowed |  |
| BillingRate | decimal(18,10) | 9 | NULL allowed |  |
| Unit | varchar(10) | 10 | NULL allowed |  |
| DateBegin | datetime | 8 | NULL allowed |  |
| DateEnd | datetime | 8 | NULL allowed |  |
| LastuserID | int | 4 | NULL allowed |  |
| LastUpdate | datetime | 8 | NULL allowed |  |
| BillingRounding | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

