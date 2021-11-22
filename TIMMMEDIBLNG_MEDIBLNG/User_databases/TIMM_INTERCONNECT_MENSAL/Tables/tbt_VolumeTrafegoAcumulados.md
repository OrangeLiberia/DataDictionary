#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT_MENSAL](../index.md) > [Tables](Tables.md) > dbo.tbt_VolumeTrafegoAcumulados

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_VolumeTrafegoAcumulados]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_VolumeTrafegoAcumulados: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | ID_DestinoTrafego | int | 4 | NOT NULL |  |
| [![Indexes IX_Report_TipoTrafego_TipoServico](../../../../Images/Index.png)](#indexes) | tipo_trafego_id | tinyint | 1 | NOT NULL |  |
|  | CallDuration_Minutos | float | 8 | NOT NULL |  |
|  | Volume_Trafego_Moeda | numeric(18,6) | 9 | NULL allowed |  |
|  | Minute_Rate | numeric(18,6) | 9 | NULL allowed |  |
|  | Tipo_Horario | varchar(max) | max | NULL allowed |  |
|  | Data_Calculo | datetime | 8 | NULL allowed |  |
| [![Indexes IX_Report_TipoTrafego_TipoServico](../../../../Images/Index.png)](#indexes) | OrigTime | datetime | 8 | NULL allowed |  |
|  | FK_WNP_ID_CllgnNumber | int | 4 | NOT NULL |  |
|  | FK_WNP_ID_CalledNumber | int | 4 | NOT NULL |  |
| [![Indexes IX_Report_TipoTrafego_TipoServico](../../../../Images/Index.png)](#indexes) | IDAgreement | bigint | 8 | NULL allowed |  |
|  | IDHubbing | bigint | 8 | NULL allowed |  |
|  | num_chamadas | int | 4 | NOT NULL |  |
|  | FK_Moeda_ID | int | 4 | NULL allowed |  |
|  | Trunk_In | varchar(50) | 50 | NULL allowed |  |
|  | Trunk_Out | varchar(50) | 50 | NULL allowed |  |
|  | Day | datetime | 8 | NOT NULL |  |
|  | FK_Central_ID | int | 4 | NOT NULL |  |
|  | Reprocessed | int | 4 | NULL allowed |  |
| [![Indexes IX_Report_TipoTrafego_TipoServico](../../../../Images/Index.png)](#indexes) | Tipo_Servico_ID | int | 4 | NULL allowed |  |
|  | SMS_Length | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

