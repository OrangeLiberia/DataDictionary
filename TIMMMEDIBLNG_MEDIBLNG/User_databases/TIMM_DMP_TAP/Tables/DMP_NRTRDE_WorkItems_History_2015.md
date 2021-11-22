#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.DMP_NRTRDE_WorkItems_History_2015

# ![Tables](../../../../Images/Table32.png) [dbo].[DMP_NRTRDE_WorkItems_History_2015]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Key IX_PK_DMP_NRTRDE_WorkItems_History_2015: WorkGroupID\WorkItemID](../../../../Images/cluster.png)](#indexes) | WorkGroupID | int | 4 | NOT NULL |  |
| [![Cluster Key IX_PK_DMP_NRTRDE_WorkItems_History_2015: WorkGroupID\WorkItemID](../../../../Images/cluster.png)](#indexes) | WorkItemID | int | 4 | NOT NULL |  |
|  | ActionType | varchar(50) | 50 | NOT NULL |  |
|  | Parameter | varchar(max) | max | NOT NULL |  |
|  | ExecState | tinyint | 1 | NOT NULL |  |
|  | Priority | int | 4 | NULL allowed |  |
|  | ScheduleTime | datetime | 8 | NULL allowed |  |
|  | InstanceNameExec | varchar(50) | 50 | NOT NULL |  |
|  | InstanceName | varchar(50) | 50 | NULL allowed |  |
|  | InsertDate | datetime | 8 | NULL allowed |  |
|  | SelectDate | datetime | 8 | NULL allowed |  |
|  | FinalPath | varchar(1000) | 1000 | NULL allowed |  |
|  | FileName | varchar(1000) | 1000 | NULL allowed |  |
|  | ExecDate | datetime | 8 | NULL allowed |  |
|  | ItemCount | int | 4 | NOT NULL | ((0)) |
|  | LastUpdate | datetime | 8 | NULL allowed |  |
|  | IDOperator | bigint | 8 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

