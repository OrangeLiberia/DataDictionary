#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TaxasCambio

# ![Tables](../../../../Images/Table32.png) [dbo].[TaxasCambio]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
| [![Primary Key PK_TAXAS_CAMBIO: IDTaxaCambio](../../../../Images/pk.png)](#indexes) | IDTaxaCambio | int | 4 | NOT NULL | 1 - 1 | NO |
|  | IDTipoMoeda | int | 4 | NOT NULL |  |  |
|  | Data_Cambio | smalldatetime | 4 | NOT NULL |  |  |
|  | Val_Tx_Cambio_Compra | float | 8 | NOT NULL |  |  |
|  | Val_Tx_Cambio_Venda | float | 8 | NOT NULL |  |  |
|  | Val_tx_Rf | float | 8 | NOT NULL |  |  |
|  | Val_tx_Usd | float | 8 | NULL allowed |  |  |
|  | DataRegisto | datetime | 8 | NOT NULL |  |  |
|  | IDUtilizador | int | 4 | NOT NULL |  |  |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

