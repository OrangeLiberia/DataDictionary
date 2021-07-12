#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgOrigDestCountry

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgOrigDestCountry]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgOrigDestCountry_1: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_AgreementDestinationDate
IX_TBrmgOrigDestCountry_Keys](../../../../Images/Index.png)](#indexes)(2) | IDAgreement | bigint | 8 | NOT NULL |  |  |
| [![Indexes IX_AgreementDestinationDate
IX_TBrmgOrigDestCountry_Keys](../../../../Images/Index.png)](#indexes)(2) | IDCCDestination | varchar(6) | 6 | NOT NULL |  |  |
| [![Indexes IX_AgreementDestinationDate
IX_TBrmgOrigDestCountry_Keys](../../../../Images/Index.png)](#indexes)(2)[![Foreign Keys FK_TBrmgOrigDestCountry_TBrmgOperatorZones: [dbo].[TBrmgOperatorZones].ZoneID](../../../../Images/fk.png)](#foreignkeys) | ZoneID | bigint | 8 | NOT NULL |  |  |
| [![Indexes IX_AgreementDestinationDate](../../../../Images/Index.png)](#indexes) | DateBegin | datetime | 8 | NULL allowed |  |  |
| [![Indexes IX_AgreementDestinationDate](../../../../Images/Index.png)](#indexes) | DateEnd | datetime | 8 | NULL allowed |  |  |
|  | LastuserID | int | 4 | NOT NULL |  |  |
|  | Lastupdate | datetime | 8 | NOT NULL |  | (getdate()) |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgOrigDestCountry_TBrmgOperatorZones | ZoneID->[[dbo].[TBrmgOperatorZones].[ZoneID]](TBrmgOperatorZones.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

