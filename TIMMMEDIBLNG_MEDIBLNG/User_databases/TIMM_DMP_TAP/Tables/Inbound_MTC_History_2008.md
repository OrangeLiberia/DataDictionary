#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_DMP_TAP](../index.md) > [Tables](Tables.md) > dbo.Inbound_MTC_History_2008

# ![Tables](../../../../Images/Table32.png) [dbo].[Inbound_MTC_History_2008]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_DMP_Inbound_MTC_History: BatchID\ID](../../../../Images/pkcluster.png)](#indexes) | BatchID | bigint | 8 | NOT NULL |
| [![Cluster Primary Key PK_DMP_Inbound_MTC_History: BatchID\ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | WF_STATE | int | 4 | NOT NULL |
|  | IDOperator | bigint | 8 | NULL allowed |
|  | IDAgreement | bigint | 8 | NULL allowed |
|  | A_MSISDN | varchar(32) | 32 | NULL allowed |
|  | A_CC | varchar(6) | 6 | NULL allowed |
|  | A_NDC | varchar(6) | 6 | NULL allowed |
|  | A_IMSI | varchar(32) | 32 | NULL allowed |
|  | A_IMEI | varchar(32) | 32 | NULL allowed |
|  | A_factur | varchar(6) | 6 | NULL allowed |
|  | A_WNP | int | 4 | NULL allowed |
|  | B_MSISDN | varchar(32) | 32 | NULL allowed |
|  | B_CC | varchar(6) | 6 | NULL allowed |
|  | B_NDC | varchar(6) | 6 | NULL allowed |
|  | B_factur | varchar(6) | 6 | NULL allowed |
|  | B_WNP | int | 4 | NULL allowed |
| [![Indexes IX_DATE_BEGIN_CALL](../../../../Images/Index.png)](#indexes) | Date_Begin_Call | datetime | 8 | NULL allowed |
|  | Date_End_Call | datetime | 8 | NULL allowed |
|  | CallDuration | int | 4 | NULL allowed |
|  | lac | int | 4 | NULL allowed |
|  | cellID | int | 4 | NULL allowed |
|  | supplServiceCode | varchar(2) | 2 | NULL allowed |
|  | supplServiceActionCode | int | 4 | NULL allowed |
|  | clirIndicator | tinyint | 1 | NULL allowed |
|  | Begin_Day_Type | varchar(2) | 2 | NULL allowed |
|  | End_Day_Type | varchar(2) | 2 | NULL allowed |
|  | Initial_Schedule_Type | int | 4 | NOT NULL |
|  | Final_Schedule_Type | int | 4 | NOT NULL |
|  | ID_Central | int | 4 | NOT NULL |
|  | Cod_BTS | int | 4 | NOT NULL |
|  | Trunk_In | int | 4 | NOT NULL |
|  | Trunk_Out | int | 4 | NULL allowed |
|  | ReleaseCause | smallint | 2 | NULL allowed |
|  | Tariff_Class | varchar(1) | 1 | NOT NULL |
|  | PriceableItem | int | 4 | NOT NULL |
|  | GrupoPI | int | 4 | NOT NULL |
|  | RatetableCod | varchar(1) | 1 | NOT NULL |
|  | rateTableID | int | 4 | NOT NULL |
|  | RateValue | numeric(18,10) | 9 | NOT NULL |
|  | RoamingRateValue | numeric(18,10) | 9 | NOT NULL |
|  | periodoMovimento | varchar(6) | 6 | NULL allowed |
|  | PrePosPago | int | 4 | NOT NULL |
|  | INProcessing | int | 4 | NOT NULL |
|  | CDR_State | int | 4 | NOT NULL |
|  | tobilling | int | 4 | NOT NULL |
|  | notbilling | int | 4 | NOT NULL |
|  | TAPRoaming_State | int | 4 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

