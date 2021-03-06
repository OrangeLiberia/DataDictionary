#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.FullCustomerBase

# ![Tables](../../../../Images/Table32.png) [fwk].[FullCustomerBase]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| MSISDN | varchar(20) | 20 | NOT NULL |  |
| SubsID | numeric(18,0) | 9 | NULL allowed |  |
| Active | bit | 1 | NOT NULL |  |
| PreActivationDT | date | 3 | NULL allowed |  |
| RegistrationDT | date | 3 | NULL allowed |  |
| BIFirstActivityDT | date | 3 | NULL allowed |  |
| BILastActivityDT | date | 3 | NULL allowed |  |
| LastCellID | smallint | 2 | NULL allowed |  |
| MostUsedCellID | smallint | 2 | NULL allowed |  |
| FirstIMEI | varchar(20) | 20 | NULL allowed | _1 if its the first IMEI used by this MSISDN_ |
| LastIMEI | varchar(20) | 20 | NULL allowed | _1 if its the last IMEI used by this MSISDN_ |
| TotalRechargesMain | decimal(18,6) | 9 | NULL allowed |  |
| TotalConsumedMain | decimal(18,6) | 9 | NULL allowed |  |
| ARPURange | tinyint | 1 | NULL allowed | _ID of the ARPU Range (see [in.ARPURanges](ARPURanges.md))_ |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[BIDMP_SUBS_FIRSTACTIVITY]](../../External/Programmability/Stored_Procedures/BIDMP_SUBS_FIRSTACTIVITY.md)
* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

