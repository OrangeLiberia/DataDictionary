#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.AcessosFeaturesBilling

# ![Tables](../../../../Images/Table32.png) [dbo].[AcessosFeaturesBilling]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_AcessosFeaturesBilling: IDAcessoFeature\FeeType](../../../../Images/pkcluster.png)](#indexes) | IDAcessoFeature | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_AcessosFeaturesBilling: IDAcessoFeature\FeeType](../../../../Images/pkcluster.png)](#indexes) | FeeType | int | 4 | NOT NULL |
|  | ActFreeMonths | int | 4 | NOT NULL |
|  | FullMonthCycle | bit | 1 | NOT NULL |
|  | RateTableCod | varchar(12) | 12 | NULL allowed |
|  | PriceableItemID | int | 4 | NOT NULL |
|  | WalletID | int | 4 | NOT NULL |
|  | PrePaidDebitMaxRetries | int | 4 | NOT NULL |
|  | PrePaidMinIntvRetries | int | 4 | NOT NULL |
|  | DebitMonthOnlyOnce | bit | 1 | NOT NULL |
|  | SendSMSSuccess | bit | 1 | NOT NULL |
|  | SMSSuccess | varchar(max) | max | NULL allowed |
|  | SendSMSError | bit | 1 | NOT NULL |
|  | SMSError | varchar(max) | max | NULL allowed |
|  | SendSMSRetry | bit | 1 | NOT NULL |
|  | SMSRetry | varchar(max) | max | NULL allowed |
|  | NDaysSendWarnSMS | tinyint | 1 | NOT NULL |
|  | SMSWarn | varchar(max) | max | NULL allowed |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NULL allowed |
|  | SSCycleMonths | int | 4 | NULL allowed |
|  | Parameters | varchar(max) | max | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

