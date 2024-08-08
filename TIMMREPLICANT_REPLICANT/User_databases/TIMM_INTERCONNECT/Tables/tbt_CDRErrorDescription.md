#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.tbt_CDRErrorDescription

# ![Tables](../../../../Images/Table32.png) [dbo].[tbt_CDRErrorDescription]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_tbt_CDRErrorDescription: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Description | varchar(100) | 100 | NOT NULL |  |
| [![Foreign Keys FK_tbt_CDRErrorDescription_ICON_CDRErrorSeverity: [dbo].[ICON_CDRErrorSeverity].SeverityID](../../../../Images/fk.png)](#foreignkeys) | SeverityID | int | 4 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_tbt_CDRErrorDescription_ICON_CDRErrorSeverity | SeverityID->[[dbo].[ICON_CDRErrorSeverity].[ID]](ICON_CDRErrorSeverity.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

