#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.Subscriptions_20170531

# ![Tables](../../../../Images/Table32.png) [dbo].[Subscriptions_20170531]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| SubscriptionID | uniqueidentifier | 16 | NOT NULL |
| OwnerID | uniqueidentifier | 16 | NOT NULL |
| Report_OID | uniqueidentifier | 16 | NOT NULL |
| Locale | nvarchar(128) | 256 | NOT NULL |
| InactiveFlags | int | 4 | NOT NULL |
| ExtensionSettings | ntext | max | NULL allowed |
| ModifiedByID | uniqueidentifier | 16 | NOT NULL |
| ModifiedDate | datetime | 8 | NOT NULL |
| Description | nvarchar(512) | 1024 | NULL allowed |
| LastStatus | nvarchar(260) | 520 | NULL allowed |
| EventType | nvarchar(260) | 520 | NOT NULL |
| MatchData | ntext | max | NULL allowed |
| LastRunTime | datetime | 8 | NULL allowed |
| Parameters | ntext | max | NULL allowed |
| DataSettings | ntext | max | NULL allowed |
| DeliveryExtension | nvarchar(260) | 520 | NULL allowed |
| Version | int | 4 | NOT NULL |
| ReportZone | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

