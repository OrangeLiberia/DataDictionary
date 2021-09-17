#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.OMBuyBundleHistory

# ![Tables](../../../../Images/Table32.png) [dbo].[OMBuyBundleHistory]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_OMBuyBundleHistory: APITransID](../../../../Images/pkcluster.png)](#indexes) | APITransID | bigint | 8 | NOT NULL | _API ID_ |
| [![Indexes IX_STDIDX](../../../../Images/Index.png)](#indexes) | APIDateTime | datetime | 8 | NOT NULL | _API Datetime_ |
| [![Indexes IX_STDIDX](../../../../Images/Index.png)](#indexes) | PayerMSISDN | varchar(32) | 32 | NOT NULL | _MSISDN of the payer of the Bundle_ |
| [![Indexes IX_STDIDX](../../../../Images/Index.png)](#indexes) | RecipientMSISDN | varchar(32) | 32 | NULL allowed | _MSISDN of the recipient of the Bundle_ |
|  | OMTransID | varchar(32) | 32 | NOT NULL | _OM Transaction ID_ |
| [![Indexes IX_STDIDX](../../../../Images/Index.png)](#indexes) | TypeActivation | int | 4 | NOT NULL | _Type of activation (10 - Myself, 20 - Other)_ |
| [![Indexes IX_STDIDX](../../../../Images/Index.png)](#indexes) | BundleID | varchar(32) | 32 | NULL allowed | _Package Bundle ID_ |
|  | Amount | decimal(18,5) | 9 | NULL allowed | _Amount_ |
|  | Currency | varchar(8) | 8 | NULL allowed | _Currency_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_OMBuyBundleHistory: APITransID](../../../../Images/pkcluster.png)](#indexes) | PK_OMBuyBundleHistory | APITransID |  | YES |
|  | IX_STDIDX | APIDateTime, TypeActivation, BundleID | PayerMSISDN, RecipientMSISDN |  |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

