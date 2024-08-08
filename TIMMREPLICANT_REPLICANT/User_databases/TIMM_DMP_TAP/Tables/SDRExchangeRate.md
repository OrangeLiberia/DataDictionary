#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.SDRExchangeRate

# ![Tables](../../../../Images/Table32.png) [dbo].[SDRExchangeRate]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SDRExchangeRate: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | Currency | varchar(50) | 50 | NOT NULL |  |
| [![Indexes IX_Date](../../../../Images/Index.png)](#indexes) | Date | datetime | 8 | NOT NULL |  |
|  | DailyRate | decimal(38,19) | 17 | NULL allowed |  |
|  | Fluctuation | tinyint | 1 | NULL allowed |  |
|  | BARGRate | decimal(38,19) | 17 | NULL allowed |  |
|  | BARGRateDate | datetime | 8 | NULL allowed |  |
|  | exchangeRateCode | int | 4 | NULL allowed |  |
|  | numberOfDecimalPlaces | int | 4 | NULL allowed |  |
|  | exchangeRate | varchar(50) | 50 | NULL allowed |  |
|  | Description | varchar(50) | 50 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

