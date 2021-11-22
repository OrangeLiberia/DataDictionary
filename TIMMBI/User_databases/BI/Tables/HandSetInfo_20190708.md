#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.HandSetInfo_20190708

# ![Tables](../../../../Images/Table32.png) [msc].[HandSetInfo_20190708]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| ID | int | 4 | NOT NULL | 1 - 1 |
| TAC | varchar(10) | 10 | NOT NULL |  |
| MarketingName | varchar(500) | 500 | NULL allowed |  |
| DesignationType | varchar(500) | 500 | NULL allowed |  |
| Manufacturer | varchar(500) | 500 | NULL allowed |  |
| Bands | varchar(3000) | 3000 | NULL allowed |  |
| AllocationDate | datetime | 8 | NULL allowed |  |
| CountryCode | varchar(10) | 10 | NULL allowed |  |
| FixedCode | varchar(10) | 10 | NULL allowed |  |
| ManufacturerCode | nvarchar(10) | 20 | NULL allowed |  |
| RadioInterface | varchar(100) | 100 | NULL allowed |  |
| 3GAndAbove | bit | 1 | NOT NULL |  |
| Brand | varchar(250) | 250 | NULL allowed |  |
| Model | varchar(250) | 250 | NULL allowed |  |
| IDHandSetStandard | int | 4 | NULL allowed |  |
| LTE | bit | 1 | NOT NULL |  |


---

## <a name="#uses"></a>Uses

* [msc]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

