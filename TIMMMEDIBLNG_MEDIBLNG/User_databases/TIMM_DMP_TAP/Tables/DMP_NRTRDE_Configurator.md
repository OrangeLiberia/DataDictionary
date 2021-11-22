#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_NRTRDE_Configurator

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_NRTRDE_Configurator]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|
| ID | int | 4 | NOT NULL | 1 - 1 |  |
| ActionOrder | int | 4 | NOT NULL |  |  |
| ActionType | varchar(50) | 50 | NOT NULL |  |  |
| ActionParameter | varchar(max) | max | NOT NULL |  |  |
| InstanceName | varchar(50) | 50 | NOT NULL |  | ('BCPOUT') |
| Enabled | bit | 1 | NOT NULL |  | ((0)) |
| ConfigType | varchar(50) | 50 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

