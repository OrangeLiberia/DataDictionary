#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.WalletRevenueMonthlySpread

# ![Tables](../../../../Images/Table32.png) [in].[WalletRevenueMonthlySpread]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_WalletRevenueMonthlySpread: IDDimDate\WalletID\Range](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int | 4 | NOT NULL |  | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| [![Cluster Primary Key PK_WalletRevenueMonthlySpread: IDDimDate\WalletID\Range](../../../../Images/pkcluster.png)](#indexes) | WalletID | tinyint | 1 | NOT NULL |  | _Wallet ID (see [in.WalletTypes](WalletTypes.md))_ |
| [![Cluster Primary Key PK_WalletRevenueMonthlySpread: IDDimDate\WalletID\Range](../../../../Images/pkcluster.png)](#indexes) | Range | varchar(30) | 30 | NOT NULL |  |  |
|  | NumberSubscribers | bigint | 8 | NOT NULL |  |  |
|  | RateBillTotal | float | 8 | NOT NULL | ((0)) |  |
|  | RateDurOnNet | float | 8 | NOT NULL | ((0)) |  |
|  | RateBillOnNet | float | 8 | NOT NULL | ((0)) |  |
|  | RateDurOffNet | float | 8 | NOT NULL | ((0)) |  |
|  | RateBillOffNet | float | 8 | NOT NULL | ((0)) |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_WalletRevenueMonthlySpread: IDDimDate\WalletID\Range](../../../../Images/pkcluster.png)](#indexes) | PK_WalletRevenueMonthlySpread | IDDimDate, WalletID, Range | YES | IN |


---

## <a name="#uses"></a>Uses

* [in]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

