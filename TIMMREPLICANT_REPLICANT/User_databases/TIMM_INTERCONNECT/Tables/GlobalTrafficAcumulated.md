#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.GlobalTrafficAcumulated

# ![Tables](../../../../Images/Table32.png) [dbo].[GlobalTrafficAcumulated]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Period | varchar(6) | 6 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Day | datetime | 8 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | ID_DestinoTrafego | int | 4 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | tipo_trafego_id | tinyint | 1 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | CallDuration_Minutos | decimal(18,4) | 9 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Volume_Trafego_Moeda | numeric(18,6) | 9 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Minute_Rate | numeric(18,6) | 9 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | FK_WNP_ID_Trunk_In | int | 4 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | FK_WNP_ID_CllgnNumber | int | 4 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | FK_WNP_ID_CalledNumber | int | 4 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | IDAgreement | bigint | 8 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | IDHubbing | bigint | 8 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Num_Calls | int | 4 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | FK_Moeda_ID | int | 4 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Trunk_In | varchar(50) | 50 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Trunk_Out | varchar(50) | 50 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | FK_Central_ID | int | 4 | NOT NULL |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | Tipo_Servico_ID | int | 4 | NULL allowed |  |
| [![Cluster Key cci_GlobalTrafficAcumulated: ID\Period\Day\ID_DestinoTrafego\tipo_trafego_id\CallDuration_Minutos\Volume_Trafego_Moeda\Minute_Rate\FK_WNP_ID_Trunk_In\FK_WNP_ID_CllgnNumber\FK_WNP_ID_CalledNumber\IDAgreement\IDHubbing\Num_Calls\FK_Moeda_ID\Trunk_In\Trunk_Out\FK_Central_ID\Tipo_Servico_ID\SMS_Length](../../../../Images/cluster.png)](#indexes) | SMS_Length | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

