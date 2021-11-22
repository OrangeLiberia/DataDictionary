#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > in.Subscribers02

# ![Tables](../../../../Images/Table32.png) [in].[Subscribers02]

---

## <a name="#description"></a>MS_Description

Subscriber Snapshot Day 02

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Subscribers02: SubsID](../../../../Images/pkcluster.png)](#indexes) | SubsID | int | 4 | NOT NULL | _IN Subscriber ID_ |
|  | SubsNumber | nvarchar(50) | 100 | NOT NULL | _Subscriber number_ |
|  | CosID | int | 4 | NOT NULL | _Class of Service ID_ |
|  | StatusID | int | 4 | NOT NULL | _Status ID_ |
|  | PrevDefiniteStatusID | int | 4 | NULL allowed | _Previous Status ID_ |
|  | CreationDate | datetime | 8 | NULL allowed | _Subscriber creation date_ |
|  | ActivationDate | datetime | 8 | NULL allowed | _Subscriber Activation date_ |
|  | StatusChangedDate | datetime | 8 | NULL allowed | _Status _ |
|  | LanguageID | int | 4 | NULL allowed | _Language ID_ |
|  | SubsPPSCounters | varchar(500) | 500 | NOT NULL |  |
|  | PersonalInfo00 | varchar(8000) | 8000 | NULL allowed |  |
|  | MSISDN | varchar(32) | 32 | NULL allowed | _Subscriber number_ |
|  | IN | tinyint | 1 | NOT NULL | _IN Identification (ref. table [BI].[in].[INs] )_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Subscribers02: SubsID](../../../../Images/pkcluster.png)](#indexes) | PK_Subscribers02 | SubsID | YES | IN |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

