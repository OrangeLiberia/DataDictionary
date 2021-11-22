#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._LogPack

# ![Tables](../../../../Images/Table32.png) [dbo].[_LogPack]

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
| DTExec | datetime | 8 | NOT NULL |  | (getdate()) |
| Msg | varchar(100) | 100 | NULL allowed |  |  |
| DTParamFirstDay | datetime | 8 | NULL allowed |  |  |
| DTParamLastDay | datetime | 8 | NULL allowed |  |  |
| DTVarFirstDay | datetime | 8 | NULL allowed |  |  |
| DTVarLastDay | datetime | 8 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

