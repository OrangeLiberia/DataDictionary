#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo._CustomerDeviceInfoBase2015Q2.06

# ![Tables](../../../../Images/Table32.png) [dbo].[_CustomerDeviceInfoBase2015Q2.06]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| MSISDN | varchar(51) | 51 | NOT NULL |
| SimType | varchar(2) | 2 | NOT NULL |
| DataService | bit | 1 | NULL allowed |
| BIFirstActivity | datetime | 8 | NULL allowed |
| BILastActivity | datetime | 8 | NULL allowed |
| BIActivityBeforeTF | bit | 1 | NULL allowed |
| BIActivityDuringTF | bit | 1 | NULL allowed |
| 4GOutOfBundle | decimal(20,5) | 13 | NULL allowed |
| 4GBundles | decimal(20,5) | 13 | NULL allowed |
| DataUpMb | numeric(18,6) | 9 | NULL allowed |
| DataDownMb | numeric(18,6) | 9 | NULL allowed |
| IDDimDate | int | 4 | NULL allowed |
| IMEI | varchar(32) | 32 | NULL allowed |
| LastIMEI | bit | 1 | NULL allowed |
| FirstMSISDN | bit | 1 | NULL allowed |
| LastMSISDN | bit | 1 | NULL allowed |
| FirstIMEI | bit | 1 | NULL allowed |
| ID | int | 4 | NULL allowed |
| TAC | varchar(10) | 10 | NULL allowed |
| Brand | varchar(250) | 250 | NULL allowed |
| Model | varchar(250) | 250 | NULL allowed |
| 3GAndAbove | bit | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

