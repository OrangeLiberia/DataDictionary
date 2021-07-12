#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.Tcom_WNP_CountryCodes

# ![Tables](../../../../Images/Table32.png) [dbo].[Tcom_WNP_CountryCodes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Tcom_WNP_CountryCodes: ID](../../../../Images/pkcluster.png)](#indexes) | ID | smallint | 2 | NOT NULL | 1 - 1 | NO |
| [![Indexes UNQ_Tcom_WNP_CountryCodes](../../../../Images/Index.png)](#indexes) | CountryCode | varchar(5) | 5 | NULL allowed |  |  |
| [![Indexes UNQ_Tcom_WNP_CountryCodes](../../../../Images/Index.png)](#indexes) | ISO-3166-1_alpha-2 | varchar(2) | 2 | NULL allowed |  |  |
| [![Indexes UNQ_Tcom_WNP_CountryCodes](../../../../Images/Index.png)](#indexes) | ISO-3166-1_alpha-3 | varchar(3) | 3 | NULL allowed |  |  |
|  | Destination | varchar(50) | 50 | NULL allowed |  |  |
|  | utc_min | numeric(9,3) | 5 | NULL allowed |  |  |
|  | utc_max | numeric(9,3) | 5 | NULL allowed |  |  |
|  | IDContinent | smallint | 2 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

