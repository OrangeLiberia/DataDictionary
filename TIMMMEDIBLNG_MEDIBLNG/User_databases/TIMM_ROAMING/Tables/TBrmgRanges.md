#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_ROAMING](../index.md) > [Tables](Tables.md) > dbo.TBrmgRanges

# ![Tables](../../../../Images/Table32.png) [dbo].[TBrmgRanges]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TBrmgRanges: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
| [![Foreign Keys FK_TBrmgRanges_TBrmgAgreements: [dbo].[TBrmgAgreements].IDAgreement](../../../../Images/fk.png)](#foreignkeys) | IDAgreement | bigint | 8 | NOT NULL |  |
|  | ImsiInicial | bigint | 8 | NOT NULL |  |
|  | ImsiFinal | bigint | 8 | NOT NULL |  |


---

## <a name="#foreignkeys"></a>Foreign Keys

| Name | Columns |
|---|---|
| FK_TBrmgRanges_TBrmgAgreements | IDAgreement->[[dbo].[TBrmgAgreements].[IDAgreement]](TBrmgAgreements.md) |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

