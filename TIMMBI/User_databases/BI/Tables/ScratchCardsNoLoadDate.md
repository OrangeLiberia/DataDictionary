#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.ScratchCardsNoLoadDate

# ![Tables](../../../../Images/Table32.png) [in].[ScratchCardsNoLoadDate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsNoLoadDate: IDDimDate\CardSerialNumber](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_ScratchCardsNoLoadDate: IDDimDate\CardSerialNumber](../../../../Images/pkcluster.png)](#indexes) | CardSerialNumber | varchar(50) | 50 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ScratchCardsNoLoadDate: IDDimDate\CardSerialNumber](../../../../Images/pkcluster.png)](#indexes) | PK_ScratchCardsNoLoadDate | IDDimDate, CardSerialNumber | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

## <a name="#usedby"></a>Used By

* [[in].[spc_TransformationScratchCardsDaily]](../Programmability/Stored_Procedures/spc_TransformationScratchCardsDaily.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

