#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.Log

# ![Tables](../../../../Images/Table32.png) [dbo].[Log]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|
| ID | int | 4 | NOT NULL | 1 - 1 |  |
| Msg | varchar(100) | 100 | NULL allowed |  |  |
| Params | varchar(100) | 100 | NULL allowed |  |  |
| DT | datetime | 8 | NULL allowed |  | (getdate()) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

