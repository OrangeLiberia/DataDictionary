#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.ICON_CDRErrorControl

# ![Tables](../../../../Images/Table32.png) [dbo].[ICON_CDRErrorControl]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ICON_CDRErrorControl: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_ICON_CDRErrorControl_Config_Central: [dbo].[Config_Central].CentralID](../../../../Images/fk.png)](#foreignkeys) | CentralID | int | 4 | NOT NULL |  |
|  | ErrorID | int | 4 | NOT NULL |  |
|  | totalDuration | int | 4 | NOT NULL |  |
|  | numCalls | int | 4 | NOT NULL |  |
|  | Day | datetime | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_ICON_CDRErrorControl_Config_Central | CentralID->[[dbo].[Config_Central].[ID]](Config_Central.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

