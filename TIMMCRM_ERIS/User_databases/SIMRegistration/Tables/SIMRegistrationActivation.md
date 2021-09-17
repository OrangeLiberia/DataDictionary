#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.SIMRegistrationActivation

# ![Tables](../../../../Images/Table32.png) [dbo].[SIMRegistrationActivation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
|  | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | IDSIMRegistration | bigint | 8 | NOT NULL |  |  |
|  | MSISDN | varchar(20) | 20 | NOT NULL |  |  |
| [![Cluster Primary Key PK_SIMRegistrationActivation: SubsID](../../../../Images/pkcluster.png)](#indexes) | SubsID | numeric(18,0) | 9 | NOT NULL |  |  |
|  | ProvDate | datetime | 8 | NOT NULL |  | (getdate()) |
|  | APP | varchar(10) | 10 | NULL allowed |  |  |
|  | UserID | int | 4 | NULL allowed |  |  |
|  | LastIDSIMRegistration | bigint | 8 | NULL allowed |  |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_SIMRegistrationActivation: SubsID](../../../../Images/pkcluster.png)](#indexes) | PK_SIMRegistrationActivation | SubsID | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

