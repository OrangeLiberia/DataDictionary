#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.TcomLanguagesINMapper

# ![Tables](../../../../Images/Table32.png) [dbo].[TcomLanguagesINMapper]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK__TcomLanguagesINMapper__10782ADC: LanguageId](../../../../Images/pkcluster.png)](#indexes) | LanguageId | int | 4 | NOT NULL |
| [![Indexes UQ__TcomLanguagesINMapper__1A019516](../../../../Images/Index.png)](#indexes) | LanguageLocale | int | 4 | NOT NULL |
|  | LanguageName | varchar(100) | 100 | NOT NULL |
|  | DataRegisto | datetime | 8 | NOT NULL |
|  | IDAccount | int | 4 | NOT NULL |
|  | rowguid | uniqueidentifier | 16 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

