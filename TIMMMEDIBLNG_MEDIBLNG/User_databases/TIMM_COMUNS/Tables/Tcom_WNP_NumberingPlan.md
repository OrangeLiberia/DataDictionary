#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.Tcom_WNP_NumberingPlan

# ![Tables](../../../../Images/Table32.png) [dbo].[Tcom_WNP_NumberingPlan]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Tcom_WNP_NumberingPlan: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 | NO |
| [![Indexes UNQ_Tcom_WNP_NumberingPlan_CNS](../../../../Images/Index.png)](#indexes) | cns | varchar(20) | 20 | NOT NULL |  |  |
|  | country_code | varchar(5) | 5 | NOT NULL |  |  |
|  | national_significant_number | varchar(20) | 20 | NOT NULL |  |  |
|  | IDParent | int | 4 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

