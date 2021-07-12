#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.VolumeTrafegoAcumulados_temp

# ![Tables](../../../../Images/Table32.png) [dbo].[VolumeTrafegoAcumulados_temp]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_VolumeTrafegoAcumulados_temp: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | TipoOTTrafego_id | int | 4 | NOT NULL |  |
|  | tipo_trafego_id | tinyint | 1 | NOT NULL |  |
|  | Volume_Trafego_Minutos | float | 8 | NOT NULL |  |
|  | Volume_Trafego_Moeda | float | 8 | NULL allowed |  |
|  | Minute_Rate | float | 8 | NULL allowed |  |
|  | Tipo_Horario | varchar(max) | max | NULL allowed |  |
|  | Data_Calculo | datetime | 8 | NULL allowed |  |
|  | Data_Registo | datetime | 8 | NULL allowed |  |
|  | CNS_Origem_ID | int | 4 | NOT NULL |  |
|  | CNS_Destino_ID | int | 4 | NOT NULL |  |
|  | Acordo_ID | bigint | 8 | NULL allowed |  |
|  | Hubbing_ID | bigint | 8 | NULL allowed |  |
|  | num_chamadas | int | 4 | NOT NULL |  |
|  | FK_Moeda_ID | int | 4 | NULL allowed |  |
|  | Trunk_In | varchar(50) | 50 | NULL allowed |  |
|  | Trunk_Out | varchar(50) | 50 | NULL allowed |  |
|  | Day | datetime | 8 | NOT NULL |  |
|  | FK_Central_ID | int | 4 | NOT NULL |  |
|  | Reprocessed | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

