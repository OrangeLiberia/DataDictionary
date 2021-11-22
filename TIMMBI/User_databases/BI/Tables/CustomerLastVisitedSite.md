#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.CustomerLastVisitedSite

# ![Tables](../../../../Images/Table32.png) [msc].[CustomerLastVisitedSite]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerLastVisitedSite: MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |  |
|  | CellID | int | 4 | NOT NULL | _Phone IMEI (imported from msc from aproximated time of CDR)_ |
|  | DateTime | datetime | 8 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerLastVisitedSite: MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerLastVisitedSite | MSISDN | YES | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[Report_QoSBarometer]](../../External/Programmability/Stored_Procedures/Report_QoSBarometer.md)
* [[External].[dbo].[Report_QoSBarometer1]](../../External/Programmability/Stored_Procedures/Report_QoSBarometer1.md)
* [[External].[dbo].[Report_QoSBarometer4]](../../External/Programmability/Stored_Procedures/Report_QoSBarometer4.md)
* [[External].[dbo].[Report_QoSBarometer5]](../../External/Programmability/Stored_Procedures/Report_QoSBarometer5.md)
* [[TIMM_Reports].[dbo].[Sanza_Campaign]](../../TIMM_Reports/Programmability/Stored_Procedures/Sanza_Campaign.md)
* [[TIMM_Reports].[dbo].[spc_trackingusersofvirantsites]](../../TIMM_Reports/Programmability/Stored_Procedures/spc_trackingusersofvirantsites.md)
* [[in].[spc_UpdateXDRLocation]](../Programmability/Stored_Procedures/spc_UpdateXDRLocation.md)
* [[msc].[spc_UpdateCustomerLastVisitedSite]](../Programmability/Stored_Procedures/spc_UpdateCustomerLastVisitedSite.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

