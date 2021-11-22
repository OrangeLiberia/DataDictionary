#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Encaminhamento

# ![Tables](../../../../Images/Table32.png) [dbo].[Encaminhamento]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_encaminhamento: ID](../../../../Images/pkcluster.png)](#indexes)[![Foreign Keys FK_Encaminhamento_Encaminhamento: [dbo].[Encaminhamento].ID](../../../../Images/fk.png)](#foreignkeys) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | idCountry | nvarchar(12) | 24 | NOT NULL |  |
|  | idOperator | bigint | 8 | NOT NULL |  |
|  | operatorType | int | 4 | NOT NULL |  |
|  | Data_Activacao | datetime | 8 | NOT NULL |  |
|  | LastUserID | nvarchar(50) | 100 | NOT NULL |  |
|  | LastChange | datetime | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Encaminhamento_Encaminhamento | ID->[[dbo].[Encaminhamento].[ID]]() |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

