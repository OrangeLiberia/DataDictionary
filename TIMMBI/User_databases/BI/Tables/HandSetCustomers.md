#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.HandSetCustomers

# ![Tables](../../../../Images/Table32.png) [msc].[HandSetCustomers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetCustomers: MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |
|  | IMEI | varchar(32) | 32 | NOT NULL |
|  | TAC | varchar(10) | 10 | NOT NULL |
|  | DateTime | datetime | 8 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetCustomers: MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_HandSetCustomers | MSISDN | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[vwc_HandSetCustomers]](../Views/vwc_HandSetCustomers.md)
* [[External].[dbo].[Report_USIM]](../../External/Programmability/Stored_Procedures/Report_USIM.md)
* [[TIMM_Reports].[dbo].[Sanza_Campaign]](../../TIMM_Reports/Programmability/Stored_Procedures/Sanza_Campaign.md)
* [[External].[dbo].[spc_AutomaticLTEUpgrade]](../../External/Programmability/Stored_Procedures/spc_AutomaticLTEUpgrade.md)
* [[in].[spc_UpdateXDRLocation]](../Programmability/Stored_Procedures/spc_UpdateXDRLocation.md)
* [[msc].[spc_LoadHandsetUsage]](../Programmability/Stored_Procedures/spc_LoadHandsetUsage.md)
* [[msc].[spc_UpdateHandsetCustomer]](../Programmability/Stored_Procedures/spc_UpdateHandsetCustomer.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

