#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgRoamingRating

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgRoamingRating]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgRoamingRating_1: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes IX_TBrmgRoamingRating_Keys](../../../../Images/Index.png)](#indexes) | IDAgreement | bigint | 8 | NOT NULL |  |
| [![Indexes IX_TBrmgRoamingRating_Keys](../../../../Images/Index.png)](#indexes)[![Foreign Keys FK_TBrmgRoamingRating_TBrmgOperatorZones: [dbo].[TBrmgOperatorZones].ZoneID](../../../../Images/fk.png)](#foreignkeys) | ZoneID | bigint | 8 | NOT NULL |  |
| [![Indexes IX_TBrmgRoamingRating_Keys](../../../../Images/Index.png)](#indexes)[![Foreign Keys FK_TBrmgRoamingRating_TBrmgOperatorSchedule: [dbo].[TBrmgOperatorSchedule].ScheduleID](../../../../Images/fk.png)](#foreignkeys)[![Foreign Keys FK_TBrmgRoamingRating_TBrmgTiposHorario: [dbo].[TBrmgTiposHorario].ScheduleID](../../../../Images/fk.png)](#foreignkeys) | ScheduleID | int | 4 | NOT NULL |  |
| [![Indexes IX_TBrmgRoamingRating_Keys](../../../../Images/Index.png)](#indexes) | Daytype | varchar(10) | 10 | NOT NULL |  |
|  | InitialInterval | int | 4 | NULL allowed |  |
|  | InitialRate | decimal(18,10) | 9 | NULL allowed |  |
|  | BillingInterval | int | 4 | NULL allowed |  |
|  | BillingRate | decimal(18,10) | 9 | NULL allowed |  |
|  | Unit | varchar(10) | 10 | NULL allowed |  |
|  | DateBegin | datetime | 8 | NULL allowed |  |
|  | DateEnd | datetime | 8 | NULL allowed |  |
|  | LastuserID | int | 4 | NULL allowed |  |
|  | LastUpdate | datetime | 8 | NULL allowed |  |
|  | BillingRounding | int | 4 | NULL allowed |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgRoamingRating_TBrmgOperatorSchedule | ScheduleID->[[dbo].[TBrmgOperatorSchedule].[ID]](TBrmgOperatorSchedule.md) |
| FK_TBrmgRoamingRating_TBrmgOperatorZones | ZoneID->[[dbo].[TBrmgOperatorZones].[ZoneID]](TBrmgOperatorZones.md) |
| FK_TBrmgRoamingRating_TBrmgTiposHorario | ScheduleID->[[dbo].[TBrmgTiposHorario].[TipoHorario]](TBrmgTiposHorario.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

