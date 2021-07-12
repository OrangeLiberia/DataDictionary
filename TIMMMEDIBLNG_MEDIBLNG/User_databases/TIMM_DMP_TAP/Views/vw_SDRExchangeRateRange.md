#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Views](Views.md) > dbo.vw_SDRExchangeRateRange

# ![Views](../../../../Images/View32.png) [dbo].[vw_SDRExchangeRateRange]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | bigint | 8 | 0 - 0 |
| DateBegin | datetime | 8 |  |
| DateEnd | datetime | 8 |  |
| dailyrate | decimal(38,19) | 17 |  |
| fluctuation | tinyint | 1 |  |
| bargrate | decimal(38,19) | 17 |  |
| bargratedate | datetime | 8 |  |
| exchangeratecode | int | 4 |  |
| numberofdecimalplaces | int | 4 |  |
| exchangerate | varchar(50) | 50 |  |
| description | varchar(50) | 50 |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

