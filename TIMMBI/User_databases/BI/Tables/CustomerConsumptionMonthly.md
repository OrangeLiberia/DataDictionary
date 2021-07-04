#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > orange.CustomerConsumptionMonthly

# ![Tables](../../../../Images/Table32.png) [orange].[CustomerConsumptionMonthly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CustomerConsumptionMonthly: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |
|  | Month | date | 3 | NOT NULL |
| [![Cluster Primary Key PK_CustomerConsumptionMonthly: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |
|  | N143SMSs | bigint | 8 | NULL allowed |
|  | N143Calls | bigint | 8 | NULL allowed |
|  | 143RealSeconds | float | 8 | NULL allowed |
|  | 143BillSeconds | float | 8 | NULL allowed |
|  | 143FeeAmount | float | 8 | NULL allowed |
|  | RechargesAmount | float | 8 | NULL allowed |
|  | NRecharges | bigint | 8 | NULL allowed |
|  | DataMB | float | 8 | NULL allowed |
|  | TotalConsumedAmount | float | 8 | NULL allowed |
|  | SMSConsumedAmount | float | 8 | NULL allowed |
|  | VoiceConsumedAmount | float | 8 | NULL allowed |
|  | DataConsumedAmount | float | 8 | NULL allowed |
|  | VoiceConsumedOnNet | float | 8 | NULL allowed |
|  | VoiceConsumedOffNet | float | 8 | NULL allowed |
|  | VoiceConsumedIntl | float | 8 | NULL allowed |
|  | SMSConsumedOnNet | float | 8 | NULL allowed |
|  | SMSConsumedOffNet | float | 8 | NULL allowed |
|  | SMSConsumedIntl | float | 8 | NULL allowed |
|  | OnNetSeconds | float | 8 | NULL allowed |
|  | OffNetSeconds | float | 8 | NULL allowed |
|  | IntlSeconds | float | 8 | NULL allowed |
|  | OnNetSMS | bigint | 8 | NULL allowed |
|  | OffNetSMS | bigint | 8 | NULL allowed |
|  | IntlSMS | bigint | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CustomerConsumptionMonthly: IDDimDate\MSISDN](../../../../Images/pkcluster.png)](#indexes) | PK_CustomerConsumptionMonthly | IDDimDate, MSISDN | YES |


---

## <a name="#uses"></a>Uses

* [orange]


---

## <a name="#usedby"></a>Used By

* [[orange].[spc_OrangeDataLoad]](../Programmability/Stored_Procedures/spc_OrangeDataLoad.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

