#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.TEMP_CDRsRoaming

# ![Tables](../../../../Images/Table32.png) [dbo].[TEMP_CDRsRoaming]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 3304245 |
| Created | 5:14:57 PM Wednesday, December 18, 2019 |
| Last Modified | 5:15:15 PM Wednesday, December 18, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Primary Key PK_CDRsRoaming : FileID\CDRID](../../../../Images/pk.png)](#indexes) | FileID | bigint | 8 | NOT NULL |  |
| [![Primary Key PK_CDRsRoaming : FileID\CDRID](../../../../Images/pk.png)](#indexes) | CDRID | int | 4 | NOT NULL |  |
|  | CallingNumber | varchar(30) | 30 | NULL allowed |  |
|  | CallingNumberCC | varchar(10) | 10 | NULL allowed |  |
|  | CallingNumberNDC | varchar(10) | 10 | NULL allowed |  |
|  | CallingNumberWNPID | bigint | 8 | NULL allowed |  |
|  | CalledNumber | varchar(30) | 30 | NULL allowed |  |
|  | CalledNumberCC | varchar(10) | 10 | NULL allowed |  |
|  | CalledNumberNDC | varchar(10) | 10 | NULL allowed |  |
|  | CalledNumberWNPID | bigint | 8 | NULL allowed |  |
|  | BillingNumber | varchar(30) | 30 | NULL allowed |  |
|  | BillingNumberIMSI | varchar(20) | 20 | NULL allowed |  |
|  | BillingNumberIMEI | varchar(20) | 20 | NULL allowed |  |
|  | BillingNumberWNPID | bigint | 8 | NULL allowed |  |
|  | ServiceID | numeric(18,0) | 9 | NULL allowed |  |
|  | AccountID | numeric(18,0) | 9 | NULL allowed |  |
|  | ProfilePlanID | int | 4 | NULL allowed |  |
|  | DateTimeStartCall | datetime | 8 | NULL allowed |  |
|  | DateTimeEndCall | datetime | 8 | NULL allowed |  |
|  | CallDurationSec | int | 4 | NULL allowed |  |
|  | INProcessing | int | 4 | NULL allowed |  |
|  | SwitchID | int | 4 | NULL allowed |  |
|  | SwitchName | varchar(10) | 10 | NULL allowed |  |
|  | ServiceType | varchar(10) | 10 | NULL allowed |  |
|  | CallingIDOrig | varchar(10) | 10 | NULL allowed |  |
|  | CalledIDDest | varchar(10) | 10 | NULL allowed |  |
|  | BillingIDOrig | varchar(10) | 10 | NULL allowed |  |
|  | DayTypeBegin | char(1) | 1 | NULL allowed |  |
|  | DayTypeEnd | char(1) | 1 | NULL allowed |  |
|  | HourTypeBegin | char(1) | 1 | NULL allowed |  |
|  | HourTypeEnd | char(1) | 1 | NULL allowed |  |
|  | TariffClass | varchar(10) | 10 | NULL allowed |  |
|  | RateTableCod | varchar(12) | 12 | NULL allowed |  |
|  | RateTableID | int | 4 | NULL allowed |  |
|  | RateValue | numeric(18,5) | 9 | NULL allowed |  |
|  | FinalValue | numeric(18,5) | 9 | NULL allowed |  |
|  | ChargeableUnits | int | 4 | NULL allowed |  |
|  | ChargedUnits | int | 4 | NULL allowed |  |
|  | AmountIN | numeric(18,5) | 9 | NULL allowed |  |
|  | EndingBalance | numeric(18,5) | 9 | NULL allowed |  |
|  | Currency | varchar(5) | 5 | NULL allowed |  |
|  | WalletID | int | 4 | NULL allowed |  |
|  | PriceableItemID | int | 4 | NULL allowed |  |
|  | GroupPriceableItemID | int | 4 | NULL allowed |  |
|  | Product | varchar(100) | 100 | NULL allowed |  |
|  | BillCycleRunID | bigint | 8 | NULL allowed |  |
|  | BillCell | int | 4 | NULL allowed |  |
|  | BillCicloFact | tinyint | 1 | NULL allowed |  |
|  | PeriodBill | varchar(6) | 6 | NULL allowed |  |
|  | PeriodMov | varchar(6) | 6 | NULL allowed |  |
|  | BTSCodeBegin | varchar(10) | 10 | NULL allowed |  |
|  | BTSCodeEnd | varchar(10) | 10 | NULL allowed |  |
|  | TrunkIn | varchar(20) | 20 | NULL allowed |  |
|  | TrunkOut | varchar(20) | 20 | NULL allowed |  |
|  | EntryTimeStamp | datetime | 8 | NOT NULL | (getdate()) |


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

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

