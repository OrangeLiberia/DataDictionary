#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.ReportsOrigDestConfig

# ![Tables](../../../../Images/Table32.png) [fwk].[ReportsOrigDestConfig]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Indexes UNQ_ReportsOrigDestConfig](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |  |
| [![Cluster Primary Key PK_ReportsOrigDestConfig: ReportName\Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | ReportName | varchar(50) | 50 | NOT NULL |  |  |  |
| [![Cluster Primary Key PK_ReportsOrigDestConfig: ReportName\Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | Type | varchar(10) | 10 | NOT NULL |  |  | _Type of the CDR (see [fwk.CallType](CallType.md))_ |
| [![Cluster Primary Key PK_ReportsOrigDestConfig: ReportName\Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | IDOrigDest | int | 4 | NOT NULL |  |  |  |
|  | IsGroup | bit | 1 | NOT NULL |  | ((0)) |  |
|  | IsTopMostGroup | bit | 1 | NOT NULL |  | ((0)) |  |
|  | IDOrigDestFinal | int | 4 | NOT NULL |  |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ReportsOrigDestConfig: ReportName\Type\IDOrigDest](../../../../Images/pkcluster.png)](#indexes) | PK_ReportsOrigDestConfig | ReportName, Type, IDOrigDest | YES | FWK |
|  | UNQ_ReportsOrigDestConfig | ID | YES | FWK |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[fwk].[fnt_ConvertReportOrigDest]](../Programmability/Functions/Scalar-valued_Functions/fnt_ConvertReportOrigDest.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

