#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.ReportDependencies

# ![Tables](../../../../Images/Table32.png) [fwk].[ReportDependencies]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ReportDependencies: IDReport\DependsOn](../../../../Images/pkcluster.png)](#indexes)[![Foreign Keys FK_ReportDependencies_IDReport: [fwk].[ETLReports].IDReport](../../../../Images/fk.png)](#foreignkeys) | IDReport | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_ReportDependencies: IDReport\DependsOn](../../../../Images/pkcluster.png)](#indexes)[![Foreign Keys FK_ReportDependencies_DependsOn: [fwk].[ETLProcess].DependsOn](../../../../Images/fk.png)](#foreignkeys) | DependsOn | int | 4 | NOT NULL |
|  | Obs | varchar(1000) | 1000 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ReportDependencies: IDReport\DependsOn](../../../../Images/pkcluster.png)](#indexes) | PK_ReportDependencies | IDReport, DependsOn | YES | FWK |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_ReportDependencies_DependsOn | DependsOn->[fwk].[ETLProcess].[ID] |
| FK_ReportDependencies_IDReport | IDReport->[fwk].[ETLReports].[ID] |


---

## <a name="#uses"></a>Uses

* [fwk].[ETLProcess]
* [fwk].[ETLReports]
* [fwk]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DisableSubscription]](../Programmability/Stored_Procedures/spc_DisableSubscription.md)
* [[fwk].[spt_DisableSubscriptions]](../Programmability/Stored_Procedures/spt_DisableSubscriptions.md)
* [[fwk].[spt_EnableSubscriptions]](../Programmability/Stored_Procedures/spt_EnableSubscriptions.md)
* [[fwk].[spt_SendETLRunDependentReports]](../Programmability/Stored_Procedures/spt_SendETLRunDependentReports.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

