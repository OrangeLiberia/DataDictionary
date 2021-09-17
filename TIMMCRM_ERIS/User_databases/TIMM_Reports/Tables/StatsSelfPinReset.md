#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.StatsSelfPinReset

# ![Tables](../../../../Images/Table32.png) [dbo].[StatsSelfPinReset]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_StatsSelfPinReset: RefDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL | _Reference date_ |
| [![Cluster Primary Key PK_StatsSelfPinReset: RefDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(10) | 10 | NOT NULL | _MSISDN_ |
|  | Currency | varchar(10) | 10 | NULL allowed | _Currency_ |
|  | AddRecoveryNumber | int | 4 | NULL allowed | _Quantity of addition actions of trusted numbers_ |
|  | RemoveContactNumber | int | 4 | NULL allowed | _Quantity of removal actions of trusted numbers_ |
|  | ViewTrustedNumber | int | 4 | NULL allowed | _Quantity of viewable actions of trusted number_ |
|  | ResetPIN | int | 4 | NULL allowed | _Quantity of reset of PINs actions _ |
|  | UsedSelfPINMenu | int | 4 | NULL allowed | _Quantity of interactions on SelfPINReset menu_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_StatsSelfPinReset: RefDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_StatsSelfPinReset | RefDate, MSISDN | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

