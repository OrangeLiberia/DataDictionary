#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.ContadorVolumeTrafego

# ![Tables](../../../../Images/Table32.png) [dbo].[ContadorVolumeTrafego]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ContadorVolumeTrafego: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | Acordo_ID | int | 4 | NOT NULL |  |  |
|  | Tipo_Trafego_ID | int | 4 | NOT NULL |  |  |
|  | Mes | int | 4 | NOT NULL |  |  |
|  | Ano | int | 4 | NOT NULL |  |  |
|  | VolumeTrafegoMin | float | 8 | NOT NULL |  | ((0)) |
|  | DataCriacao | smalldatetime | 4 | NOT NULL |  | (getdate()) |
|  | DataUltrapassouLimite | smalldatetime | 4 | NULL allowed |  |  |
|  | DataUltimaActualizacao | smalldatetime | 4 | NOT NULL |  | (getdate()) |
|  | Origem_Trafego_ID | int | 4 | NOT NULL |  |  |
|  | Destino_Trafego_ID | int | 4 | NOT NULL |  |  |
|  | Tipo_Servico_ID | int | 4 | NULL allowed |  |  |
|  | TipoRate_id | int | 4 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

