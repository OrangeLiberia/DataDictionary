#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Central_Provincia

# ![Tables](../../../../Images/Table32.png) [dbo].[Central_Provincia]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Central_Provincia: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_Central_Provincia_Config_Central: [dbo].[Config_Central].ID_central](../../../../Images/fk.png)](#foreignkeys) | ID_central | int | 4 | NOT NULL |  |
|  | FK_TComProvincias | int | 4 | NOT NULL |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Central_Provincia_Config_Central | ID_central->[[dbo].[Config_Central].[ID]](Config_Central.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

