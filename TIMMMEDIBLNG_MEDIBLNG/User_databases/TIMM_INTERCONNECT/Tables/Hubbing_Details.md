#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Hubbing_Details

# ![Tables](../../../../Images/Table32.png) [dbo].[Hubbing_Details]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Hubbing_Details: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 17126 - 1 |
|  | custosHubbingID | int | 4 | NOT NULL |  |
|  | Country | varchar(500) | 500 | NULL allowed |  |
|  | Destination | varchar(500) | 500 | NULL allowed |  |
|  | Type | varchar(max) | max | NULL allowed |  |
|  | NumberingPlan | varchar(max) | max | NULL allowed |  |
|  | Price | numeric(18,6) | 9 | NULL allowed |  |
|  | StartDate | datetime | 8 | NOT NULL |  |
|  | mes_inicio | int | 4 | NOT NULL |  |
|  | WNP_RangeCreated | tinyint | 1 | NULL allowed |  |
|  | CountryCode | varchar(500) | 500 | NULL allowed |  |
|  | IDCountryCode | int | 4 | NULL allowed |  |
|  | EndDate | datetime | 8 | NULL allowed |  |
|  | LastUserUpdate | int | 4 | NULL allowed |  |
|  | LastDateUpdate | datetime | 8 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

