#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Operadoras

# ![Tables](../../../../Images/Table32.png) [dbo].[Operadoras]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_operadoras: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |
| [![Indexes IX_STD_SEEK](../../../../Images/Index.png)](#indexes) | operadoras_country_id | int | 4 | NOT NULL |  |  |
|  | designacao | varchar(200) | 200 | NOT NULL |  |  |
|  | contabancaria | varchar(500) | 500 | NULL allowed |  |  |
| [![Indexes IX_STD_SEEK](../../../../Images/Index.png)](#indexes) | operator_system | bit | 1 | NOT NULL |  |  |
|  | contactos | xml | max | NOT NULL |  |  |
|  | Morada | varchar(500) | 500 | NULL allowed |  |  |
|  | Localidade | varchar(100) | 100 | NULL allowed |  |  |
|  | Zip_Code | varchar(15) | 15 | NULL allowed |  |  |
|  | NIPC | varchar(50) | 50 | NULL allowed |  |  |
| [![Indexes IX_STD_SEEK](../../../../Images/Index.png)](#indexes) | TcomOperadora_id | bigint | 8 | NULL allowed |  |  |
|  | operadoras_logo | image | max | NULL allowed |  |  |
|  | lastuserupdate | int | 4 | NOT NULL |  |  |
|  | lastdateupdate | datetime | 8 | NOT NULL |  |  |
|  | tipo_operadora | varchar(50) | 50 | NOT NULL |  | ('FIXMOB') |
|  | deleted | bit | 1 | NOT NULL |  | ((0)) |
|  | BillingATT | varchar(250) | 250 | NULL allowed |  |  |
|  | BalanceATT | varchar(250) | 250 | NULL allowed |  |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

