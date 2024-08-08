#### 

[Project](../../../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../../../index.md) > [User databases](../../../../index.md) > [DW_OrangeMoney](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Table-valued Functions](Table-valued_Functions.md) > dbo.tvf_KPI_Operations_Active

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[tvf_KPI_Operations_Active]

## <a name="#description"></a>MS_Description

Provides the Active Operational KPIs begin the timespan [@dtBegin, @dtEnd[.

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @dtBegin | date | 3 |
| @dtEnd | date | 3 |


## <a name="#ReturnedDataset"></a>Returned Dataset
| Name | Data Type | Description |
|---|---|---|
| ActiveCashIN | int | Total number of distinct active customers for Cash-In transactions. |
| ActiveCashOUT | int | Total number of distinct active customers for Cash-Out transactions. |
| ActiveP2P | int | Total number of distinct active customers for P2P transactions. |
| ActiveTNO | int | Total number of distinct active customers performing transactions to Non-Orange numbers. |
| ActiveTOPUP | int | Total number of distinct active customers performing Airtime top-ups transactions. |
| ActiveOrangeBundle | int | Total number of distinct active customers performing Orange Bundle transactions. |
| ActiveBillPayment | int | Total number of distinct active customers performing Bill payment [insurance, food delivery,...] transactions. |
| ActiveMerchantPayment | int | Total number of distinct active customers performing Merchant payment transactions. |
| ActiveSalaryPayment | int | Total number of distinct active customers performing Salary payments transactions. |
| ActiveB2WIN | int | Total number of distinct active customers performing Bank-to-Wallet transactions. |
| ActiveB2WOUT | int | Total number of distinct active customers performing Wallet-to-Bank transactions. |
| ActiveIRTIN | int | Total number of distinct active customers performing inbound International Remitance transactions. |
| ActiveIRTOUT | int | Total number of distinct active customers performing outbound International Remitance transactions. |
| ActiveP2G | int | Total number of distinct active customers performing Person-to-Goverment transactions. |
| ActiveBetting_OUT | int | Total number of distinct active customers performing online betting "OUT" transactions (reimbursements) (reimbursements from betting company to customer). |
| ActiveBetting_IN | int | Total number of distinct active customers performing online betting "IN" transactions (payments) (payments from customer to betting company). |
| ActiveElectricity | int | Total number of distinct active customers performing LEC transactions. |
| ActiveTV | int | Total number of distinct active customers paying for TV transactions. |
| ActiveMerchants | int | Total number of distinct active merchants accepting payments for goods and services. |
| ActiveOrangeEnergy | int | Total number of distinct active customers performing Orange Energy transactions. |
---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

