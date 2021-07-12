#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgAgreements

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgAgreements]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default |
|---|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgAgreements: IDAgreement](../../../../Images/pkcluster.png)](#indexes)[![Indexes IX_LastClosedAgreements
IX_AgreemntDate
ix_TBrmgAgreements_PLMNIDParentOperator_DateBegin](../../../../Images/Index.png)](#indexes)(3) | IDAgreement | bigint | 8 | NOT NULL | 1 - 1 |  |
|  | AgreementName | varchar(200) | 200 | NULL allowed |  |  |
|  | Version | varchar(10) | 10 | NULL allowed |  |  |
| [![Indexes ix_TBrmgAgreements_PLMNIDParentOperator_DateBegin](../../../../Images/Index.png)](#indexes) | IDHomeOperator | int | 4 | NOT NULL |  |  |
|  | AgreementType | varchar(10) | 10 | NULL allowed |  |  |
|  | IDOperator | int | 4 | NOT NULL |  |  |
| [![Indexes ix_TBrmgAgreements_PLMNIDParentOperator_DateBegin](../../../../Images/Index.png)](#indexes) | IDParentOperator | int | 4 | NULL allowed |  |  |
| [![Indexes IX_AgreemntDate
ix_TBrmgAgreements_PLMNIDParentOperator_DateBegin](../../../../Images/Index.png)](#indexes)(2) | PLMNIDParentOperator | varchar(5) | 5 | NULL allowed |  |  |
| [![Indexes IX_LastClosedAgreements](../../../../Images/Index.png)](#indexes)[![Foreign Keys FK_TBrmgAgreements_TBrmgStatus: [dbo].[TBrmgStatus].AgreementStatusID](../../../../Images/fk.png)](#foreignkeys) | AgreementStatusID | int | 4 | NULL allowed |  |  |
| [![Indexes IX_AgreemntDate
ix_TBrmgAgreements_PLMNIDParentOperator_DateBegin](../../../../Images/Index.png)](#indexes)(2) | DateBegin | datetime | 8 | NULL allowed |  |  |
| [![Indexes IX_LastClosedAgreements
IX_AgreemntDate
ix_TBrmgAgreements_PLMNIDParentOperator_DateBegin](../../../../Images/Index.png)](#indexes)(3) | DateEnd | datetime | 8 | NULL allowed |  |  |
|  | TaxesApplied | int | 4 | NULL allowed |  |  |
|  | TipoMoedaID | int | 4 | NULL allowed |  |  |
|  | LastuserID | int | 4 | NOT NULL |  |  |
|  | Lastupdate | datetime | 8 | NOT NULL |  | (getdate()) |
|  | RatingType | varchar(20) | 20 | NOT NULL |  | ('DLYRT') |
|  | PLMNIDHomeOperator | varchar(7) | 7 | NULL allowed |  |  |
| [![Indexes IX_LastClosedAgreements](../../../../Images/Index.png)](#indexes) | PLMNIDOperator | varchar(7) | 7 | NULL allowed |  |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgAgreements_TBrmgStatus | AgreementStatusID->[[dbo].[TBrmgStatus].[ID]](TBrmgStatus.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

