#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.SalesData

# ![Tables](../../../../Images/Table32.png) [dbo].[SalesData]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 508 |
| Created | 10:43:40 AM Monday, August 16, 2021 |
| Last Modified | 10:43:40 AM Monday, August 16, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | int | 4 | NOT NULL | 1 - 1 |
| SaleDate | date | 3 | NULL allowed |  |
| SalesAmount | decimal(10,2) | 9 | NULL allowed |  |
| ProductName | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#usedby"></a>Used By

* [dbo].[SPX_RESET_SALES_DATA]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

