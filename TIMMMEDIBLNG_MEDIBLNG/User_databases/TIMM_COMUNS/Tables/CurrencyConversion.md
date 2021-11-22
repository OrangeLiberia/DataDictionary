#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.CurrencyConversion

# ![Tables](../../../../Images/Table32.png) [dbo].[CurrencyConversion]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CurrencyConversion: ID_Origem\ID_Destino\DataInicio](../../../../Images/pkcluster.png)](#indexes) | ID_Origem | int | 4 | NOT NULL |  |  |
| [![Cluster Primary Key PK_CurrencyConversion: ID_Origem\ID_Destino\DataInicio](../../../../Images/pkcluster.png)](#indexes) | ID_Destino | int | 4 | NOT NULL |  |  |
|  | NSequence | int | 4 | NOT NULL | 1 - 1 | NO |
| [![Cluster Primary Key PK_CurrencyConversion: ID_Origem\ID_Destino\DataInicio](../../../../Images/pkcluster.png)](#indexes) | DataInicio | datetime | 8 | NOT NULL |  |  |
|  | DataFim | datetime | 8 | NULL allowed |  |  |
|  | Taxa | decimal(38,19) | 17 | NOT NULL |  |  |
|  | LastUpdate | datetime | 8 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

