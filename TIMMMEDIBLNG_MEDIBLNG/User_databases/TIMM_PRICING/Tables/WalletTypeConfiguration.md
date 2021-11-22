#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.WalletTypeConfiguration

# ![Tables](../../../../Images/Table32.png) [dbo].[WalletTypeConfiguration]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_WalletTypeConfiguration: WalletTypeID](../../../../Images/pkcluster.png)](#indexes) | WalletTypeID | int | 4 | NOT NULL | 1 - 1 | NO |
|  | WalletTypeName | varchar(max) | max | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NULL allowed |  |  |
|  | LastUserID | int | 4 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

