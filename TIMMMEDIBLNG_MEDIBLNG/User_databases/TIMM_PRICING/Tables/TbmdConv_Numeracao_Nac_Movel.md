#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdConv_Numeracao_Nac_Movel

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdConv_Numeracao_Nac_Movel]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbmdConv_Numeracao_Nac_Movel: Codigo\Digitos](../../../../Images/pkcluster.png)](#indexes) | Codigo | varchar(10) | 10 | NOT NULL |
|  | Designacao | varchar(200) | 200 | NOT NULL |
|  | CodNDCMovel | int | 4 | NOT NULL |
|  | CodNormalizado | varchar(10) | 10 | NOT NULL |
|  | CodOrigDest | varchar(10) | 10 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
| [![Cluster Primary Key PK_TbmdConv_Numeracao_Nac_Movel: Codigo\Digitos](../../../../Images/pkcluster.png)](#indexes) | Digitos | tinyint | 1 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

