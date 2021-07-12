#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.CosWalletConfiguration

# ![Tables](../../../../Images/Table32.png) [dbo].[CosWalletConfiguration]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CosWalletConfiguration: CosID\WalletID](../../../../Images/pkcluster.png)](#indexes) | CosID | varchar(64) | 64 | NOT NULL |
| [![Cluster Primary Key PK_CosWalletConfiguration: CosID\WalletID](../../../../Images/pkcluster.png)](#indexes) | WalletID | int | 4 | NOT NULL |
|  | WalletName | varchar(256) | 256 | NULL allowed |
|  | CurrencyID | int | 4 | NOT NULL |
|  | CurrencyAbrv | varchar(20) | 20 | NOT NULL |
|  | WalletTypeID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

