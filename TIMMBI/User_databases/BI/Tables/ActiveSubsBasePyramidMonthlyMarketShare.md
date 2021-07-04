#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBasePyramidMonthlyMarketShare

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBasePyramidMonthlyMarketShare]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBasePyramidMonthlyMarketShare: IDDimDate](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | NSubsCustomerBase | int | 4 | NULL allowed |
|  | NSubsOffNetMTN | int | 4 | NULL allowed |
|  | NSubsOnNet | int | 4 | NULL allowed |
|  | NSubsMTN | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBasePyramidMonthlyMarketShare: IDDimDate](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBasePyramidMonthlyMarketShare | IDDimDate | YES |


---

## <a name="#usedby"></a>Used By

* [[TIMM_Reports].[dbo].[spr_KPIOrangeMarketShare]](../../TIMM_Reports/Programmability/Stored_Procedures/spr_KPIOrangeMarketShare.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

