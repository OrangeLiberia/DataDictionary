#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_PRICING](../index.md) > [Tables](Tables.md) > dbo.TbmdConv_Numeracao_Nac_Fixa

# ![Tables](../../../../Images/Table32.png) [dbo].[TbmdConv_Numeracao_Nac_Fixa]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TbmdConv_Numeracao_Nac_Fixa: Codigo](../../../../Images/pkcluster.png)](#indexes) | Codigo | varchar(10) | 10 | NOT NULL |
|  | Designacao | varchar(200) | 200 | NOT NULL |
|  | CodNDCFixa | int | 4 | NOT NULL |
|  | CodOrigDest | varchar(10) | 10 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | Digitos | tinyint | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

