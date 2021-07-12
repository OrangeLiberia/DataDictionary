#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.CAMEL_Roaming

# ![Tables](../../../../Images/Table32.png) [dbo].[CAMEL_Roaming]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CAMEL_Roaming: FileID\CDRID\RefDate](../../../../Images/pkcluster.png)](#indexes) | FileID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_CAMEL_Roaming: FileID\CDRID\RefDate](../../../../Images/pkcluster.png)](#indexes) | CDRID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_CAMEL_Roaming: FileID\CDRID\RefDate](../../../../Images/pkcluster.png)](#indexes) | RefDate | date | 3 | NOT NULL |
| [![Indexes IX_CAMEL_Roaming_CalledGT](../../../../Images/Index.png)](#indexes) | CalledGT | varchar(512) | 512 | NULL allowed |
|  | SubsNumber | varchar(32) | 32 | NULL allowed |
|  | SubsNumber_NDC | varchar(2) | 2 | NOT NULL |
|  | SubsNumber_CC | varchar(3) | 3 | NOT NULL |
|  | SubsNumber_OrigDest | int | 4 | NOT NULL |
|  | SubsNumber_WNPID | int | 4 | NOT NULL |
|  | DialedDigits | varchar(512) | 512 | NULL allowed |
|  | CalledNumber | varchar(32) | 32 | NULL allowed |
|  | B_NDC | varchar(16) | 16 | NULL allowed |
|  | B_CC | varchar(16) | 16 | NULL allowed |
|  | B_WNPID | int | 4 | NULL allowed |
|  | Answer_Time | datetime | 8 | NULL allowed |
|  | Disconnect_Time | datetime | 8 | NULL allowed |
|  | Chargeable_Duration | decimal(28,0) | 13 | NULL allowed |
|  | Origem_factur | varchar(4) | 4 | NOT NULL |
|  | Destino_OrigDest | varchar(16) | 16 | NULL allowed |
|  | Ending_Balance | decimal(28,6) | 13 | NULL allowed |
|  | Amount_Charged | decimal(28,6) | 13 | NULL allowed |
|  | MainWalletCharge | decimal(28,6) | 13 | NULL allowed |
|  | ServiceType | varchar(5) | 5 | NOT NULL |
|  | Type | varchar(16) | 16 | NULL allowed |
|  | Zone | varchar(512) | 512 | NULL allowed |
|  | EVENT_PARAMETER9 | varchar(512) | 512 | NULL allowed |
|  | COS_ID | int | 4 | NULL allowed |
|  | WALLET_TYPE_ID | int | 4 | NULL allowed |
|  | PRODUCT_TYPE | decimal(28,0) | 13 | NULL allowed |
|  | SubsType | varchar(5) | 5 | NULL allowed |
| [![Indexes IX_CAMEL_Roaming_PLMNID](../../../../Images/Index.png)](#indexes) | PLMNID | varchar(8) | 8 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

