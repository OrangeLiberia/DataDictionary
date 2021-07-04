#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.SUBSCOUNTYVOICEDATA

# ![Tables](../../../../Images/Table32.png) [dbo].[SUBSCOUNTYVOICEDATA]

---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__SUBSCOUN__28BF303A39970331: KEYID](../../../../Images/pkcluster.png)](#indexes) | KEYID | int | 4 | NOT NULL | 1 - 1 |
|  | CURRENTMONTH | varchar(10) | 10 | NULL allowed |  |
|  | MSISDN | varchar(10) | 10 | NULL allowed |  |
|  | CellID | varchar(10) | 10 | NULL allowed |  |
|  | DATAUSAGE | numeric(10,9) | 9 | NULL allowed |  |
|  | VOICEUSAGE | numeric(10,9) | 9 | NULL allowed |  |
|  | COUNTY | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__SUBSCOUN__28BF303A39970331: KEYID](../../../../Images/pkcluster.png)](#indexes) | PK__SUBSCOUN__28BF303A39970331 | KEYID | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

