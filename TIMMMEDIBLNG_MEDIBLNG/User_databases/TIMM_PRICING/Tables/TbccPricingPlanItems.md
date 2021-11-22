#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccPricingPlanItems

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccPricingPlanItems]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccPricingPlanItems: PricingPlanID\TarifClasse](../../../../Images/pkcluster.png)](#indexes) | PricingPlanID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_TbccPricingPlanItems: PricingPlanID\TarifClasse](../../../../Images/pkcluster.png)](#indexes) | TarifClasse | varchar(10) | 10 | NOT NULL |
|  | RateTableCod | varchar(12) | 12 | NOT NULL |
|  | PrePosPago | tinyint | 1 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

