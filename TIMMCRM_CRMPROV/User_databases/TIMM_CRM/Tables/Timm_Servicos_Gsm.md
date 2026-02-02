#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Tables](Tables.md) > dbo.Timm_Servicos_Gsm

# ![Tables](../../../../Images/Table32.png) [dbo].[Timm_Servicos_Gsm]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Identity Replication |
|---|---|---|---|---|---|---|
|  | ID | int | 4 | NOT NULL | 1 - 1 | NO |
| [![Cluster Primary Key PK_TbCrmServicos_GSM: IMEI](../../../../Images/pkcluster.png)](#indexes) | IMEI | numeric(19,0) | 9 | NOT NULL |  |  |
| [![Indexes IX_TbCrmServicos_GSM](../../../../Images/Index.png)](#indexes) | MCC | varchar(3) | 3 | NOT NULL |  |  |
| [![Indexes IX_TbCrmServicos_GSM](../../../../Images/Index.png)](#indexes) | MNC | varchar(2) | 2 | NOT NULL |  |  |
| [![Indexes IX_TbCrmServicos_GSM](../../../../Images/Index.png)](#indexes) | IMSI | varchar(10) | 10 | NOT NULL |  |  |
|  | MSISDN | varchar(50) | 50 | NULL allowed |  |  |
|  | Entidade | numeric(18,0) | 9 | NULL allowed |  |  |
|  | Status | tinyint | 1 | NOT NULL |  |  |
|  | LastUserID | int | 4 | NULL allowed |  |  |
|  | Created_At | datetime | 8 | NOT NULL |  |  |
|  | Updated_At | datetime | 8 | NOT NULL |  |  |
|  | PUK1 | varchar(8) | 8 | NULL allowed |  |  |
|  | PUK2 | varchar(8) | 8 | NULL allowed |  |  |
|  | PIN1 | varchar(8) | 8 | NULL allowed |  |  |
|  | PIN2 | varchar(8) | 8 | NULL allowed |  |  |
|  | KI | nvarchar(400) | 800 | NULL allowed |  |  |
|  | ICCID | varchar(18) | 18 | NULL allowed |  |  |
|  | KIENC | tinyint | 1 | NOT NULL |  |  |
|  | TipoCartaoID | int | 4 | NOT NULL |  |  |
|  | OPC | varchar(50) | 50 | NULL allowed |  |  |
|  | AuthTypeID | int | 4 | NOT NULL |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

