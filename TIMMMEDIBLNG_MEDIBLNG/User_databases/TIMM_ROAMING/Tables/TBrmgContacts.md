#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgContacts

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgContacts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgContacts: IDrmgContact](../../../../Images/pkcluster.png)](#indexes) | IDrmgContact | int | 4 | NOT NULL | 1 - 1 |  |
|  | IDOperator | int | 4 | NULL allowed |  |  |
| [![Foreign Keys FK_TBrmgContacts_TBrmgContactType: [dbo].[TBrmgContactType].ContactType](../../../../Images/fk.png)](#foreignkeys) | ContactType | int | 4 | NULL allowed |  |  |
|  | IDSupervisor | int | 4 | NULL allowed |  |  |
|  | Name | varchar(50) | 50 | NULL allowed |  |  |
|  | PhoneNumber | varchar(50) | 50 | NULL allowed |  |  |
|  | MobileNumber | varchar(50) | 50 | NULL allowed |  |  |
|  | FaxNumber | varchar(50) | 50 | NULL allowed |  |  |
|  | EMailAddress | varchar(50) | 50 | NULL allowed |  |  |
|  | SIPAddress | varchar(100) | 100 | NULL allowed |  |  |
|  | PostAddress | varchar(100) | 100 | NULL allowed |  |  |
|  | PostalCode | varchar(50) | 50 | NULL allowed |  |  |
|  | CountryCode | varchar(10) | 10 | NULL allowed |  |  |
|  | LastuserID | int | 4 | NULL allowed |  |  |
|  | Lastupdate | datetime | 8 | NULL allowed |  | (getdate()) |
|  | status | bit | 1 | NULL allowed |  | ((1)) |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgContacts_TBrmgContactType | ContactType->[[dbo].[TBrmgContactType].[ID]](TBrmgContactType.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

