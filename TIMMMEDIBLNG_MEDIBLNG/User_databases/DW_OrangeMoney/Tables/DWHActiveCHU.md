#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.DWHActiveCHU

# ![Tables](../../../../Images/Table32.png) [dbo].[DWHActiveCHU]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Is Partitioned | YES |
| Partitioned Column | RefDate |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DWHActiveCHUv1: *](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_DWHActiveCHUv1: *](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_DWHActiveCHUv1: *](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
|  | CurrencyType | varchar(16) | 16 | NULL allowed |
|  | MSISDN | varchar(60) | 60 | NULL allowed |
|  | USER_ID | varchar(32) | 32 | NULL allowed |
|  | USERNAME | varchar(80) | 80 | NULL allowed |
|  | LAST_NAME | varchar(80) | 80 | NULL allowed |
|  | CATEGORY_CODE | varchar(20) | 20 | NULL allowed |
|  | TRANSACTION_TYPE | varchar(10) | 10 | NULL allowed |
|  | SERVICE_TYPE | varchar(10) | 10 | NULL allowed |
|  | LAST_TRANSFER_DATE | datetime | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | Partition Scheme | Partitioned |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DWHActiveCHUv1: *](../../../../Images/pkcluster.png)](#indexes) | PK_DWHActiveCHUv1 | FileID, ID, RefDate | YES | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

