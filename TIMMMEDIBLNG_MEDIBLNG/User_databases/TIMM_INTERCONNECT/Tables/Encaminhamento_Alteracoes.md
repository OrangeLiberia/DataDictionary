#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.Encaminhamento_Alteracoes

# ![Tables](../../../../Images/Table32.png) [dbo].[Encaminhamento_Alteracoes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_encaminhamento_Alteracoes: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_Encaminhamento_Alteracoes_Encaminhamento: [dbo].[Encaminhamento].FK_idEncaminhamento](../../../../Images/fk.png)](#foreignkeys) | FK_idEncaminhamento | bigint | 8 | NOT NULL |  |
| [![Foreign Keys FK_Encaminhamento_Alteracoes_Alteracoes: [dbo].[Rotas].FK_idRota](../../../../Images/fk.png)](#foreignkeys) | FK_idRota | int | 4 | NOT NULL |  |
|  | Preference | int | 4 | NOT NULL |  |
|  | Data_Activacao | datetime | 8 | NOT NULL |  |
|  | LastUserID | nvarchar(50) | 100 | NOT NULL |  |
|  | LastChange | datetime | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_Encaminhamento_Alteracoes_Alteracoes | FK_idRota->[[dbo].[Rotas].[ID]](Rotas.md) |
| FK_Encaminhamento_Alteracoes_Encaminhamento | FK_idEncaminhamento->[[dbo].[Encaminhamento].[ID]](Encaminhamento.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

