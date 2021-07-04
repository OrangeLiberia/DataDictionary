#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > dbo.ActiveSubsBasePyramidMonthly

# ![Tables](../../../../Images/Table32.png) [dbo].[ActiveSubsBasePyramidMonthly]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Primary Key PK_ActiveSubsBasePyramidMonthly: IDDimDate](../../../../Images/pk.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | NSubsActive | int | 4 | NULL allowed |
|  | NSubsMOCalls | int | 4 | NULL allowed |
|  | NSubsMOSMS | int | 4 | NULL allowed |
|  | NSubsHData | int | 4 | NULL allowed |
|  | NSubsVAS | int | 4 | NULL allowed |
|  | NSubsRoamingMO | int | 4 | NULL allowed |
|  | NSubsOM | int | 4 | NULL allowed |
|  | NSubsOutEvent | int | 4 | NULL allowed |
|  | NSubsMTCalls | int | 4 | NULL allowed |
|  | NSubsMTSMS | int | 4 | NULL allowed |
|  | NSubsRoamingMT | int | 4 | NULL allowed |
|  | NSubsIncEvent | int | 4 | NULL allowed |
|  | KPIGrossAdd | int | 4 | NULL allowed |
|  | KPIClosingBase | int | 4 | NULL allowed |
|  | KPIOpeningBase | int | 4 | NULL allowed |
|  | KPIAverageClosingBase | int | 4 | NULL allowed |
|  | KPIChargedBase | int | 4 | NULL allowed |
|  | KPITotalBase | int | 4 | NULL allowed |
|  | KPIDisconnection | int | 4 | NULL allowed |
|  | KPINetAdd | int | 4 | NULL allowed |
|  | KPIReconnection | int | 4 | NULL allowed |
|  | KPITotalDisconnections | int | 4 | NULL allowed |
|  | KPIAcquisionChurn | int | 4 | NULL allowed |
|  | KPIFakeAcquision | int | 4 | NULL allowed |
|  | KPIGratuityChurn | int | 4 | NULL allowed |
|  | KPIStructuralChurn | int | 4 | NULL allowed |
|  | KPIMonthlyChurnRate | decimal(18,6) | 9 | NULL allowed |
|  | KPIAnnualizedMonthlyChurnRate | decimal(18,6) | 9 | NULL allowed |
|  | KPIYtDChurnRate | decimal(18,6) | 9 | NULL allowed |
|  | KPITotalDisconnectionsChurn | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_ActiveSubsBasePyramidMonthly: IDDimDate](../../../../Images/pk.png)](#indexes) | PK_ActiveSubsBasePyramidMonthly | IDDimDate | YES |


---

## <a name="#usedby"></a>Used By

* [[TIMM_Reports].[dbo].[spr_KPIOMEARules]](../../TIMM_Reports/Programmability/Stored_Procedures/spr_KPIOMEARules.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

