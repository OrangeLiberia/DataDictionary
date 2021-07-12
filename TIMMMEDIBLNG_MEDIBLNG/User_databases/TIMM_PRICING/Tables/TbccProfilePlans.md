#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbccProfilePlans

# ![Tables](../../../../Images/Table32.png) [dbo].[TbccProfilePlans]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbccProfilePlans: ProfilePlanID](../../../../Images/pkcluster.png)](#indexes) | ProfilePlanID | int | 4 | NOT NULL |
|  | ProfilePlanCod | varchar(12) | 12 | NOT NULL |
|  | ProfilePlanDesc | varchar(200) | 200 | NOT NULL |
|  | PricingPlanID | int | 4 | NOT NULL |
|  | ThreshPlanID | int | 4 | NULL allowed |
|  | Status | tinyint | 1 | NOT NULL |
|  | DataEfectiva | datetime | 8 | NOT NULL |
|  | TipoServico | tinyint | 1 | NOT NULL |
|  | CredMensalINDefault | int | 4 | NOT NULL |
|  | DesactCicloLimitDefault | int | 4 | NOT NULL |
|  | PlanfondCredDefault | int | 4 | NOT NULL |
|  | PrePosTotal | tinyint | 1 | NOT NULL |
|  | TipoProfile | tinyint | 1 | NULL allowed |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | PrazoPagamento | int | 4 | NOT NULL |
|  | CS5 | varchar(6) | 6 | NULL allowed |
|  | TempoPermanencia | smallint | 2 | NULL allowed |
|  | AgenciaFilialID | numeric(18,0) | 9 | NULL allowed |
|  | MMProfilePlanID | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

