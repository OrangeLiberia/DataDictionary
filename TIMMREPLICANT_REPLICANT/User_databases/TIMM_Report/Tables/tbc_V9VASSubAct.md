#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.tbc_V9VASSubAct

# ![Tables](../../../../Images/Table32.png) [dbo].[tbc_V9VASSubAct]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 1467468987 |
| Created | 2:33:25 PM Thursday, January 30, 2020 |
| Last Modified | 9:59:03 AM Wednesday, February 24, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL | _Day_ |
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | TDRID | int | 4 | NOT NULL | _ID of the TDR (see [dbo.tbc_TDRID](tbc_TDRID.md))_ |
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | MSISDN | char(9) | 9 | NOT NULL | _MSISDN of the subscriber_ |
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | OriginateTime | datetime | 8 | NOT NULL | _Date and time of the event_ |
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | Value | decimal(18,6) | 9 | NOT NULL | _Amount of the transaction_ |
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | ClearCause | varchar(10) | 10 | NOT NULL | _Clear Cause of the transaction_ |
| [![Cluster Key cci_V9VASSubAct: ReferenceDay\TDRID\MSISDN\OriginateTime\Value\ClearCause\SubsType](../../../../Images/cluster.png)](#indexes) | SubsType | varchar(5) | 5 | NULL allowed | _Type of the subscriber B2B or B2C_ |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | SELECT | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | SELECT | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | SELECT | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | SELECT | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | SELECT | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwt_VASV9PerMSISDN]](../Views/vwt_VASV9PerMSISDN.md)
* [dbo].[spc_OnlineSales]
* [dbo].[spc_ProcessV9VAS]
* [dbo].[spc_VASDailyFees]
* [dbo].[spc_VASMonthlyPyramid]
* [TIMM_Reports].[dbo].[VASB2BReport]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

