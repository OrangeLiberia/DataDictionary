#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.DWHActiveSubs

# ![Tables](../../../../Images/Table32.png) [dbo].[DWHActiveSubs]

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
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | ID | int | 4 | NOT NULL |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | CurrencyType | varchar(16) | 16 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | MSISDN | varchar(60) | 60 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | USER_ID | varchar(32) | 32 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | USERNAME | varchar(80) | 80 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | LAST_NAME | varchar(80) | 80 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | CATEGORY_CODE | varchar(20) | 20 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | TRANSACTION_TYPE | varchar(10) | 10 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | SERVICE_TYPE | varchar(10) | 10 | NULL allowed |
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | LAST_TRANSFER_DATE | datetime | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Included Columns | Type | Compression | Page Locks | Row Locks | Partition Scheme | Partitioned |
|---|---|---|---|---|---|---|---|---|
| [![Cluster Key cci_DWHActiveSubsv1: *](../../../../Images/cluster.png)](#indexes) | cci_DWHActiveSubsv1 | FileID, ID, RefDate, CurrencyType, MSISDN, USER_ID, USERNAME, LAST_NAME, CATEGORY_CODE, TRANSACTION_TYPE, SERVICE_TYPE, LAST_TRANSFER_DATE | Columnstore | COLUMNSTORE ON PARTITIONS (1), COLUMNSTORE ON PARTITIONS (2), COLUMNSTORE ON PARTITIONS (3), COLUMNSTORE ON PARTITIONS (4), COLUMNSTORE ON PARTITIONS (5), COLUMNSTORE ON PARTITIONS (6), COLUMNSTORE ON PARTITIONS (7), COLUMNSTORE ON PARTITIONS (8), COLUMNSTORE ON PARTITIONS (9), COLUMNSTORE ON PARTITIONS (10), COLUMNSTORE ON PARTITIONS (11), COLUMNSTORE ON PARTITIONS (12), COLUMNSTORE ON PARTITIONS (13) | NO | NO | pschSemesterPartition | RefDate |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

