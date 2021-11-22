#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > orange.CustomerUsageDaily

# ![Tables](../../../../Images/Table32.png) [orange].[CustomerUsageDaily]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Indexes IX_CustomerUsageDaily](../../../../Images/Index.png)](#indexes) | Day | date | 3 | NULL allowed |
| [![Indexes IX_CustomerUsageDaily](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(50) | 50 | NULL allowed |
|  | SCRechargesTimes | int | 4 | NULL allowed |
|  | SCRechargesAmount | decimal(38,2) | 17 | NULL allowed |
|  | OtherRechargesTimes | int | 4 | NULL allowed |
|  | OtherRechargesAmount | decimal(38,2) | 17 | NULL allowed |
|  | 143Purchases | int | 4 | NULL allowed |
|  | 143Amount | decimal(38,2) | 17 | NULL allowed |
|  | OtherPurchases | int | 4 | NULL allowed |
|  | OtherPurchasesAmount | decimal(38,2) | 17 | NULL allowed |
|  | N143SMSs | bigint | 8 | NULL allowed |
|  | N143Calls | bigint | 8 | NULL allowed |
|  | 143Seconds | bigint | 8 | NULL allowed |
|  | DataPAYGAmount | decimal(38,2) | 17 | NULL allowed |
|  | DataBundleAmount | decimal(38,2) | 17 | NULL allowed |
|  | VoiceConsumedOnNet | decimal(38,2) | 17 | NULL allowed |
|  | VoiceConsumedOffNet | decimal(38,2) | 17 | NULL allowed |
|  | VoiceConsumedIntl | decimal(38,2) | 17 | NULL allowed |
|  | SMSConsumedOnNet | decimal(38,2) | 17 | NULL allowed |
|  | SMSConsumedOffNet | decimal(38,2) | 17 | NULL allowed |
|  | SMSConsumedIntl | decimal(38,2) | 17 | NULL allowed |
|  | OnNetMins | decimal(15,1) | 9 | NULL allowed |
|  | OffNetMins | decimal(15,1) | 9 | NULL allowed |
|  | IntlMins | decimal(15,1) | 9 | NULL allowed |
|  | OnNetSMS | bigint | 8 | NULL allowed |
|  | OffNetSMS | bigint | 8 | NULL allowed |
|  | IntlSMS | bigint | 8 | NULL allowed |
|  | DataMB | decimal(38,2) | 17 | NULL allowed |
|  | USAVoiceCalls | int | 4 | NULL allowed |
|  | IntlUSAMins | decimal(38,2) | 17 | NULL allowed |
|  | IntlUSASMSs | int | 4 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_CustomerUsageDaily | Day, MSISDN |


---

## <a name="#uses"></a>Uses

* [orange]


---

## <a name="#usedby"></a>Used By

* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

