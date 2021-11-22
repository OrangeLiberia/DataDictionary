#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.VolumeSMS_SemAcordo

# ![Tables](../../../../Images/Table32.png) [dbo].[VolumeSMS_SemAcordo]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_VolumeSMS: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | direction_id | tinyint | 1 | NOT NULL |  |
|  | SMS_Rate | float | 8 | NULL allowed |  |
|  | Data_Calculo | datetime | 8 | NULL allowed |  |
|  | Data_Registo | datetime | 8 | NULL allowed |  |
|  | CNS_Origem_ID | int | 4 | NOT NULL |  |
|  | CNS_Destino_ID | int | 4 | NOT NULL |  |
|  | Acordo_ID | bigint | 8 | NULL allowed |  |
|  | num_SMS | int | 4 | NOT NULL |  |
|  | FK_Moeda_ID | int | 4 | NULL allowed |  |
|  | Trunk_In | varchar(50) | 50 | NULL allowed |  |
|  | Trunk_Out | varchar(50) | 50 | NULL allowed |  |
|  | FK_Central_ID | int | 4 | NOT NULL |  |
|  | FK_FileDesc_ID | bigint | 8 | NULL allowed |  |
|  | FileID | bigint | 8 | NULL allowed |  |
|  | CDRID | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

