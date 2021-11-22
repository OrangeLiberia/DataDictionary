#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > msc.HandSetCustomersMonthly1

# ![Tables](../../../../Images/Table32.png) [msc].[HandSetCustomersMonthly1]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetCustomersMonthly1: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_HandSetCustomersMonthly1_IMEI
IX_HandSetCustomersMonthly1_MSISDN](../../../../Images/Index.png)](#indexes)(2) | IDDimDate | int | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_HandSetCustomersMonthly1: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_HandSetCustomersMonthly1_MSISDN](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(32) | 32 | NOT NULL |  |  |
| [![Cluster Primary Key PK_HandSetCustomersMonthly1: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_HandSetCustomersMonthly1_IMEI](../../../../Images/Index.png)](#indexes) | IMEI | varchar(32) | 32 | NOT NULL |  |  |
|  | LastIMEI | bit | 1 | NOT NULL | ((0)) | _1 if its the last IMEI used by this MSISDN_ |
|  | FirstMSISDN | bit | 1 | NOT NULL | ((0)) | _1 if its the first MSISDN used by this IMEI_ |
|  | LastMSISDN | bit | 1 | NOT NULL | ((0)) | _1 if its the last MSISDN used by this IMEI_ |
|  | FirstIMEI | bit | 1 | NOT NULL | ((0)) | _1 if its the first IMEI used by this MSISDN_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_HandSetCustomersMonthly1: IDDimDate\MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes) | PK_HandSetCustomersMonthly1 | IDDimDate, MSISDN, IMEI | YES | MSC |
|  | IX_HandSetCustomersMonthly1_IMEI | IMEI, IDDimDate |  | MSC |
|  | IX_HandSetCustomersMonthly1_MSISDN | MSISDN, IDDimDate |  | MSC |


---

## <a name="#uses"></a>Uses

* [msc]


---

## <a name="#usedby"></a>Used By

* [[msc].[HandSetCustomersMonthly]](../Views/HandSetCustomersMonthly.md)
* [[fwk].[spc_DeleteBeforeRun]](../Programmability/Stored_Procedures/spc_DeleteBeforeRun.md)
* [[msc].[spc_LoadHandsetUsage]](../Programmability/Stored_Procedures/spc_LoadHandsetUsage.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

