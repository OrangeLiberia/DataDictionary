#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Views](Views.md) > dbo.VolumeTrafegoAcumulados

# ![Views](../../../../Images/View32.png) [dbo].[VolumeTrafegoAcumulados]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | bigint | 8 | 0 - 0 |
| TipoOTTrafego_id | int | 4 |  |
| tipo_trafego_id | tinyint | 1 |  |
| Volume_Trafego_Minutos | float | 8 |  |
| Volume_Trafego_Moeda | numeric(18,6) | 9 |  |
| Minute_Rate | numeric(18,6) | 9 |  |
| Tipo_Horario | varchar(max) | max |  |
| Data_Calculo | datetime | 8 |  |
| Data_Registo | datetime | 8 |  |
| CNS_Origem_ID | int | 4 |  |
| CNS_Destino_ID | int | 4 |  |
| Acordo_ID | bigint | 8 |  |
| Hubbing_ID | bigint | 8 |  |
| num_chamadas | int | 4 |  |
| FK_Moeda_ID | int | 4 |  |
| Trunk_In | varchar(50) | 50 |  |
| Trunk_Out | varchar(50) | 50 |  |
| Day | datetime | 8 |  |
| FK_Central_ID | int | 4 |  |
| Reprocessed | int | 4 |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

