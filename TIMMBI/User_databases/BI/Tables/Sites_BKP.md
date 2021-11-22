#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.Sites_BKP

# ![Tables](../../../../Images/Table32.png) [msc].[Sites_BKP]

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
| Name | varchar(100) | 100 | NULL allowed |  |
| County | varchar(100) | 100 | NULL allowed |  |
| Location | varchar(50) | 50 | NULL allowed |  |
| UnifiedCellID | int | 4 | NULL allowed |  |
| Latitude | numeric(10,6) | 9 | NOT NULL |  |
| Longitude | numeric(10,6) | 9 | NOT NULL |  |
| SpatialData | geography | max | NOT NULL |  |
| CellsHosted | varchar(500) | 500 | NULL allowed |  |
| UnifiedSiteName | nvarchar(4000) | 8000 | NULL allowed |  |
| UnifiedSiteNameLong | nvarchar(4000) | 8000 | NULL allowed |  |


---

## <a name="#uses"></a>Uses

* [msc]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

