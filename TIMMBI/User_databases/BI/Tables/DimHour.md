#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.DimHour

# ![Tables](../../../../Images/Table32.png) [fwk].[DimHour]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_DimHourIDHour: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | Hour | tinyint | 1 | NOT NULL |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique | File Group |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DimHourIDHour: ID](../../../../Images/pkcluster.png)](#indexes) | PK_DimHourIDHour | ID | YES | FWK |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[External].[dbo].[spr_DestinationsByHour]](../../External/Programmability/Stored_Procedures/spr_DestinationsByHour.md)
* [[in].[spc_GetCallsHourly]](../Programmability/Stored_Procedures/spc_GetCallsHourly.md)
* [[in].[spt_LoadCallsDistHourly]](../Programmability/Stored_Procedures/spt_LoadCallsDistHourly.md)
* [[fwk].[fnt_GetIDDimHour]](../Programmability/Functions/Scalar-valued_Functions/fnt_GetIDDimHour.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

