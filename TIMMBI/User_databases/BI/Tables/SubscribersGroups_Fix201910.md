#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > in.SubscribersGroups_Fix201910

# ![Tables](../../../../Images/Table32.png) [in].[SubscribersGroups_Fix201910]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|
| IDDimDate | int | 4 | NOT NULL | _Date ID (see [fwk.DimDate](DimDate.md))_ |
| IDOrig | int | 4 | NULL allowed | _ID of the Calling Number (see [fwk.CallsOrigDest](CallsOrigDest.md))_ |
| MSISDN | varchar(32) | 32 | NOT NULL |  |
| RateBill | float | 8 | NULL allowed |  |
| IDRange | varchar(30) | 30 | NULL allowed | _ID of the ARPU Range (see [in.ARPURanges](ARPURanges.md))_ |
| Range | varchar(30) | 30 | NULL allowed |  |


---

## <a name="#uses"></a>Uses

* [in]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

