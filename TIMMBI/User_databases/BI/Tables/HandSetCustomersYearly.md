#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.HandSetCustomersYearly

# ![Tables](../../../../Images/Table32.png) [msc].[HandSetCustomersYearly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetCustomersYearly: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_HandSetCustomersYearly_IMEI
IX_HandSetCustomersYearly_MSISDN](../../../../Images/Index.png)](#indexes)(2) | IDDimDate | int | 4 | NOT NULL |  |
| [![Cluster Primary Key PK_HandSetCustomersYearly: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_HandSetCustomersYearly_MSISDN](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |  |
| [![Cluster Primary Key PK_HandSetCustomersYearly: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_HandSetCustomersYearly_IMEI](../../../../Images/Index.png)](#indexes) | IMEI | varchar(32) | 32 | NOT NULL |  |
|  | LastIMEI | bit | 1 | NOT NULL | ((0)) |
|  | FirstMSISDN | bit | 1 | NOT NULL | ((0)) |
|  | LastMSISDN | bit | 1 | NOT NULL | ((0)) |
|  | FirstIMEI | bit | 1 | NOT NULL | ((0)) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetCustomersYearly: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes) | PK_HandSetCustomersYearly | IDDimDate, MSISDN, IMEI | YES | MSC |
|  | IX_HandSetCustomersYearly_IMEI | IMEI, IDDimDate |  | MSC |
|  | IX_HandSetCustomersYearly_MSISDN | MSISDN, IDDimDate |  | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_LoadHandsetUsage]](../Programmability/Stored_Procedures/spc_LoadHandsetUsage.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

