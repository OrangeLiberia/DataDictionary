#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.causeForTerm

# ![Tables](../../../../Images/Table32.png) [dbo].[causeForTerm]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_causeForTerm: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | KeyCodeLang | nvarchar(250) | 500 | NULL allowed |
|  | Description | varchar(60) | 60 | NULL allowed |
|  | TAPValid | tinyint | 1 | NULL allowed |
|  | MOC | tinyint | 1 | NULL allowed |
|  | MTC | tinyint | 1 | NULL allowed |
|  | GPRS | tinyint | 1 | NULL allowed |
|  | WLAN | tinyint | 1 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

