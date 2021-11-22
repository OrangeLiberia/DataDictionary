#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.CDRsFileSeq_History

# ![Tables](../../../../Images/Table32.png) [dbo].[CDRsFileSeq_History]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| PLMNID | varchar(7) | 7 | NOT NULL |
| FileSeq | int | 4 | NOT NULL |
| Data | datetime | 8 | NULL allowed |
| Status | tinyint | 1 | NULL allowed |
| LastUpdate | datetime | 8 | NULL allowed |
| LastUserID | int | 4 | NULL allowed |
| PLMNIDHomeOperator | varchar(7) | 7 | NULL allowed |
| TipoAcordo | varchar(1) | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

