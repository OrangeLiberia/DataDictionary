#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.SIMRegistrationPictures

# ![Tables](../../../../Images/Table32.png) [dbo].[SIMRegistrationPictures]

---

## <a name="#description"></a>MS_Description

SIM Registration Pictures

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Description |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key Pk_SIMRegistrationPictures: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 | _ID_ |
|  | PictureFile | varchar(100) | 100 | NULL allowed |  | _Picture filename_ |
|  | Picture | image | max | NULL allowed |  | _Picture_ |
| [![Check Constraints CHK_SimRegPic_Picture : ([Type]='OTHER' OR [Type]='CONTRACT' OR [Type]='IDCARD' OR [Type]='FRONT')](../../../../Images/c-constraint.png)](#checkconstraints) | Type | varchar(10) | 10 | NOT NULL |  | _Type of picture (Front, IDCard, Contract)_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key Pk_SIMRegistrationPictures: ID](../../../../Images/pkcluster.png)](#indexes) | Pk_SIMRegistrationPictures | ID | YES | MEDIA |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

