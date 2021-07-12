#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.tcomServicosEligibility

# ![Tables](../../../../Images/Table32.png) [dbo].[tcomServicosEligibility]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_tcomServiceEligibility: EligibilityID](../../../../Images/pkcluster.png)](#indexes) | EligibilityID | int | 4 | NOT NULL |
|  | EligibilityCod | varchar(32) | 32 | NOT NULL |
|  | EligibilityDesc | varchar(200) | 200 | NOT NULL |
|  | DataRequirements | int | 4 | NULL allowed |
|  | Tipo | int | 4 | NOT NULL |
|  | Status | tinyint | 1 | NOT NULL |
|  | IDPermission | int | 4 | NULL allowed |
|  | APIFunction | varchar(64) | 64 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

