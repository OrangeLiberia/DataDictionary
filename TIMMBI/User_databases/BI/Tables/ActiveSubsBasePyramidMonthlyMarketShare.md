#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBasePyramidMonthlyMarketShare

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBasePyramidMonthlyMarketShare]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBasePyramidMonthlyMarketShare: IDDimDate](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
|  | NSubsCustomerBase | int | 4 | NULL allowed |  |
|  | NSubsOffNetMTN | int | 4 | NULL allowed |  |
|  | NSubsOnNet | int | 4 | NULL allowed |  |
|  | NSubsMTN | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBasePyramidMonthlyMarketShare: IDDimDate](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBasePyramidMonthlyMarketShare | IDDimDate | YES |


---

## <a name="#usedby"></a>Used By

* [[TIMM_Reports].[dbo].[spr_KPIOrangeMarketShare]](../../TIMM_Reports/Programmability/Stored_Procedures/spr_KPIOrangeMarketShare.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

