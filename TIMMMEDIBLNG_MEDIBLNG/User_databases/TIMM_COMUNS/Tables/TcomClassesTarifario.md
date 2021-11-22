#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomClassesTarifario

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomClassesTarifario]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TcomClassesTarifario: Codigo](../../../../Images/pkcluster.png)](#indexes) | Codigo | varchar(10) | 10 | NOT NULL |
|  | Designacao | varchar(200) | 200 | NOT NULL |
|  | Status | int | 4 | NOT NULL |
|  | DataEfectiva | datetime | 8 | NOT NULL |
|  | GrupoClasseTarifario | varchar(10) | 10 | NOT NULL |
|  | LastUserID | int | 4 | NOT NULL |
|  | LastUpdate | datetime | 8 | NOT NULL |
|  | IDBillingServiceType | int | 4 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

