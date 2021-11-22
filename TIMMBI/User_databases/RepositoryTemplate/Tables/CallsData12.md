#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > msc.CallsData12

# ![Tables](../../../../Images/Table32.png) [msc].[CallsData12]

---

## <a name="#description"></a>MS_Description

MSC Data Calls Day 12

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| FileID | bigint | 8 | NOT NULL | _Mediation File ID_ |
| CDRID | int | 4 | NOT NULL | _Mediation CDR ID_ |
| ServedMSISDN | varchar(32) | 32 | NULL allowed | _Subscriber Number_ |
| IMSI | varchar(17) | 17 | NULL allowed | _IMSI_ |
| IMEI | varchar(17) | 17 | NULL allowed | _IMEI_ |
| LocationAreaCode | varchar(7) | 7 | NULL allowed | _Location area code_ |
| CellIdentifier | varchar(17) | 17 | NULL allowed | _Cell ID of the Call_ |
| systemType | tinyint | 1 | NULL allowed | _System Type_ |
| changeTime | datetime | 8 | NULL allowed | _Change time_ |
| recordOpeningTime | datetime | 8 | NULL allowed | _Data record opening time_ |
| Duration | int | 4 | NULL allowed | _Duration_ |
| DataUp | bigint | 8 | NULL allowed | _Data Upload count (bytes)_ |
| DataDown | bigint | 8 | NULL allowed | _Data Download count (bytes)_ |
| AMSISDN | varchar(20) | 20 | NULL allowed | _MSISDN_ |
| IDOrig | int | 4 | NULL allowed | _A MSISDN classification_ |
| StartTime | datetime | 8 | NULL allowed | _Start time_ |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

