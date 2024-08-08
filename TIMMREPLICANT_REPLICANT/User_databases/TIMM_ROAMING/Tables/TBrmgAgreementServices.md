#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgAgreementServices

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgAgreementServices]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Default |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgAgreementServices: IDAgreement\IDServiceType](../../../../Images/pkcluster.png)](#indexes)[![Foreign Keys FK_TBrmgAgreementServices_TBrmgAgreement: [dbo].[TBrmgAgreements].IDAgreement](../../../../Images/fk.png)](#foreignkeys) | IDAgreement | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_TBrmgAgreementServices: IDAgreement\IDServiceType](../../../../Images/pkcluster.png)](#indexes)[![Foreign Keys FK_TBrmgAgreementServices_TBrmgServiceTypes: [dbo].[TBrmgServiceTypes].IDServiceType](../../../../Images/fk.png)](#foreignkeys) | IDServiceType | int | 4 | NOT NULL |  |
|  | Status | int | 4 | NULL allowed | ((0)) |
|  | LastuserID | int | 4 | NULL allowed |  |
|  | Lastupdate | datetime | 8 | NOT NULL | (getdate()) |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgAgreementServices_TBrmgAgreement | IDAgreement->[[dbo].[TBrmgAgreements].[IDAgreement]](TBrmgAgreements.md) |
| FK_TBrmgAgreementServices_TBrmgServiceTypes | IDServiceType->[[dbo].[TBrmgServiceTypes].[ID]](TBrmgServiceTypes.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

