#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.Outbound_GPRS_CHARGEINFORMATIONLIST

# ![Tables](../../../../Images/Table32.png) [dbo].[Outbound_GPRS_CHARGEINFORMATIONLIST]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST: FileDescriptorID\CDRid\ChargeInformationID](../../../../Images/pkcluster.png)](#indexes) | FileDescriptorID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST: FileDescriptorID\CDRid\ChargeInformationID](../../../../Images/pkcluster.png)](#indexes) | CDRid | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST: FileDescriptorID\CDRid\ChargeInformationID](../../../../Images/pkcluster.png)](#indexes) | ChargeInformationID | int | 4 | NOT NULL |
|  | chargedItem | varchar(2) | 2 | NULL allowed |
|  | exchangeRateCode | int | 4 | NULL allowed |
|  | callTypeLevel1 | int | 4 | NULL allowed |
|  | taxCode | int | 4 | NULL allowed |
|  | taxValue | decimal(18,6) | 9 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

