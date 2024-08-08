#### 

[Project](../../../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../../../index.md) > [User databases](../../../../index.md) > [DW_OrangeMoney](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Table-valued Functions](Table-valued_Functions.md) > dbo.tvf_KPI_Subscribers_New

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[tvf_KPI_Subscribers_New]

## <a name="#description"></a>MS_Description

Provides the count of new Subscribers for the begin the timespan [@dtBegin, @dtEnd[.


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @dtBegin | date | 3 |
| @dtEnd | date | 3 |
| @Currency | varchar(3) | 3 |


## <a name="#ReturnedDataset"></a>Returned Dataset
| Name | Data Type | Description |
|---|---|---|
| NewSubscriber | int | Count of new subscribers |

---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

