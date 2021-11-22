#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.Outbound_GPRS_CHARGEINFORMATIONLIST_CHARGEDETAILLIST

# ![Tables](../../../../Images/Table32.png) [dbo].[Outbound_GPRS_CHARGEINFORMATIONLIST_CHARGEDETAILLIST]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST_CHARGEDETAILLIST: FileDescriptorID\CDRid\ChargeInformationID\ChargeDetailID](../../../../Images/pkcluster.png)](#indexes) | FileDescriptorID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST_CHARGEDETAILLIST: FileDescriptorID\CDRid\ChargeInformationID\ChargeDetailID](../../../../Images/pkcluster.png)](#indexes) | CDRid | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST_CHARGEDETAILLIST: FileDescriptorID\CDRid\ChargeInformationID\ChargeDetailID](../../../../Images/pkcluster.png)](#indexes) | ChargeInformationID | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_Outbound_GPRS_CHARGEINFORMATIONLIST_CHARGEDETAILLIST: FileDescriptorID\CDRid\ChargeInformationID\ChargeDetailID](../../../../Images/pkcluster.png)](#indexes) | ChargeDetailID | int | 4 | NOT NULL |
|  | chargeType | varchar(2) | 2 | NULL allowed |
|  | charge | decimal(18,6) | 9 | NULL allowed |
|  | chargeableUnits | bigint | 8 | NULL allowed |
|  | chargedUnits | bigint | 8 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

