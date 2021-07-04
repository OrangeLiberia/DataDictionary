#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.HandSetInfo

# ![Tables](../../../../Images/Table32.png) [msc].[HandSetInfo]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Indexes IX_HandSetInfo](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Cluster Primary Key PK_HandSetInfo: TAC](../../../../Images/pkcluster.png)](#indexes) | TAC | varchar(10) | 10 | NOT NULL |  |  |
|  | MarketingName | varchar(500) | 500 | NULL allowed |  |  |
|  | DesignationType | varchar(500) | 500 | NULL allowed |  |  |
|  | Manufacturer | varchar(500) | 500 | NULL allowed |  |  |
|  | Bands | varchar(5000) | 5000 | NULL allowed |  |  |
|  | AllocationDate | datetime | 8 | NULL allowed |  |  |
|  | CountryCode | varchar(10) | 10 | NULL allowed |  |  |
|  | FixedCode | varchar(10) | 10 | NULL allowed |  |  |
|  | ManufacturerCode | nvarchar(10) | 20 | NULL allowed |  |  |
|  | RadioInterface | varchar(100) | 100 | NULL allowed |  |  |
|  | 3GAndAbove | bit | 1 | NOT NULL |  | ((0)) |
|  | Brand | varchar(250) | 250 | NULL allowed |  |  |
|  | Model | varchar(250) | 250 | NULL allowed |  |  |
| [![Foreign Keys FK_HandSetInfo_IDHandSetStandard: [msc].[HandSetStandard].IDHandSetStandard](../../../../Images/fk.png)](#foreignkeys) | IDHandSetStandard | int | 4 | NULL allowed |  |  |
|  | LTE | bit | 1 | NOT NULL |  | ((0)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetInfo: TAC](../../../../Images/pkcluster.png)](#indexes) | PK_HandSetInfo | TAC | YES | MSC |
|  | IX_HandSetInfo | ID |  | MSC |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_HandSetInfo_IDHandSetStandard | IDHandSetStandard->[[msc].[HandSetStandard].[ID]](HandSetStandard.md) |


---

## <a name="#uses"></a>Uses

* [[msc].[HandSetStandard]](HandSetStandard.md)
* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[vwc_HandSetCustomers]](../Views/vwc_HandSetCustomers.md)
* [[External].[dbo].[Report_USIM]](../../External/Programmability/Stored_Procedures/Report_USIM.md)
* [[External].[dbo].[spc_AutomaticLTEUpgrade]](../../External/Programmability/Stored_Procedures/spc_AutomaticLTEUpgrade.md)
* [[msc].[spc_LoadHandsetUsage]](../Programmability/Stored_Procedures/spc_LoadHandsetUsage.md)
* [[msc].[spc_UpdateHandsetCustomer]](../Programmability/Stored_Procedures/spc_UpdateHandsetCustomer.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

