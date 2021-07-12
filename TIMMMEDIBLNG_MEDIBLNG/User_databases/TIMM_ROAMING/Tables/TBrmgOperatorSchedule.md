#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgOperatorSchedule

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgOperatorSchedule]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgOperatorSchedule: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
|  | IDAgreement | bigint | 8 | NOT NULL |  |  |
| [![Foreign Keys FK_TBrmgOperatorSchedule_TBrmgTiposHorario: [dbo].[TBrmgTiposHorario].ScheduleType](../../../../Images/fk.png)](#foreignkeys) | ScheduleType | int | 4 | NOT NULL |  |  |
|  | BeginHour | varchar(6) | 6 | NOT NULL |  |  |
|  | EndHour | varchar(6) | 6 | NOT NULL |  |  |
|  | DateBegin | datetime | 8 | NULL allowed |  |  |
|  | DateEnd | datetime | 8 | NULL allowed |  |  |
|  | LastuserID | int | 4 | NOT NULL |  |  |
|  | Lastupdate | datetime | 8 | NOT NULL |  | (getdate()) |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgOperatorSchedule_TBrmgTiposHorario | ScheduleType->[[dbo].[TBrmgTiposHorario].[TipoHorario]](TBrmgTiposHorario.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

