#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._CustomerDeviceBase2015Q4.12

# ![Tables](../../../../Images/Table32.png) [dbo].[_CustomerDeviceBase2015Q4.12]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
|  | ServicoID | numeric(18,0) | 9 | NOT NULL |
| [![Indexes IX_CustomerDeviceBase2015Q412](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(51) | 51 | NOT NULL |
|  | SimType | varchar(2) | 2 | NOT NULL |
|  | DataService | tinyint | 1 | NULL allowed |
|  | BIFirstActivity | datetime | 8 | NULL allowed |
|  | BILastActivity | datetime | 8 | NULL allowed |
|  | BIActivityBeforeTF | bit | 1 | NULL allowed |
|  | BIActivityDuringTF | bit | 1 | NULL allowed |
|  | 4GOutOfBundle | decimal(20,5) | 13 | NULL allowed |
|  | 4GBundles | decimal(20,5) | 13 | NULL allowed |
|  | DataUpMb | numeric(18,6) | 9 | NULL allowed |
|  | DataDownMb | numeric(18,6) | 9 | NULL allowed |
| [![Indexes IX_CustomerDeviceBase2015Q412](../../../../Images/Index.png)](#indexes) | IDDimDate | int | 4 | NULL allowed |
| [![Indexes IX_CustomerDeviceBase2015Q412](../../../../Images/Index.png)](#indexes) | IMEI | varchar(32) | 32 | NULL allowed |
|  | LastIMEI | bit | 1 | NULL allowed |
|  | FirstMSISDN | bit | 1 | NULL allowed |
|  | LastMSISDN | bit | 1 | NULL allowed |
|  | FirstIMEI | bit | 1 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_CustomerDeviceBase2015Q412 | MSISDN, IMEI, IDDimDate |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

