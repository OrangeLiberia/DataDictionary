#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.SMSSIMRegSteps

# ![Tables](../../../../Images/Table32.png) [dbo].[SMSSIMRegSteps]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_SMSSIMRegSteps: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_SMSSIMRegSteps](../../../../Images/Index.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |  |  |
|  | PhoneNumber | varchar(20) | 20 | NULL allowed |  |  |
|  | Name | varchar(200) | 200 | NULL allowed |  |  |
|  | Gender | varchar(10) | 10 | NULL allowed |  |  |
|  | IDCard | varchar(50) | 50 | NULL allowed |  |  |
|  | IDCardType | varchar(50) | 50 | NULL allowed |  |  |
|  | DTBirthDate | datetime | 8 | NULL allowed |  |  |
|  | StrBirthDate | varchar(50) | 50 | NULL allowed |  |  |
|  | Address | varchar(200) | 200 | NULL allowed |  |  |
|  | NRetries | int | 4 | NULL allowed |  |  |
|  | NInteractions | int | 4 | NULL allowed |  |  |
|  | Status | varchar(20) | 20 | NULL allowed |  |  |
|  | PrevStatus | varchar(20) | 20 | NULL allowed |  |  |
|  | SMSReceived | varchar(200) | 200 | NULL allowed |  |  |
|  | SMSSentIndex | int | 4 | NULL allowed |  |  |
|  | SMSSent | varchar(200) | 200 | NULL allowed |  |  |
| [![Indexes IX_SMSSIMRegSteps](../../../../Images/Index.png)](#indexes) | DTLastInteraction | datetime | 8 | NOT NULL |  | (getdate()) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_SMSSIMRegSteps: ID](../../../../Images/pkcluster.png)](#indexes) | PK_SMSSIMRegSteps | ID | YES |
|  | IX_SMSSIMRegSteps | MSISDN, DTLastInteraction |  |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

