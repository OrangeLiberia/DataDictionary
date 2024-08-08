#### 

[Project](../../../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../../../index.md) > [User databases](../../../../index.md) > [DW_OrangeMoney](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Table-valued Functions](Table-valued_Functions.md) > dbo.tvf_KPI_Operations_PerDay

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[tvf_KPI_Operations_PerDay]

## <a name="#description"></a>MS_Description

Provides Operational KPIs grouped by day for begin the timespan [@dtBegin, @dtEnd[ for a specific @Currency (LRD,USD). Currency if passed as NULL will return the data for both currencies.

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
| RefDate | datetime | Reference date|
| CurrencyType | varchar(16) | Currency (USD,LRD)|
| Num_CashIN | int | Total number of successful cash-in transactions |
| Num_CashOUT | int | Total number of successful cash-out transactions |
| Num_P2P | int | Total number of successful P2P transactions |
| Num_P2pNoReg | int | Total number of successful transfer to non Orange transactions |
| Num_Airtime | int | Total amount of successful top-up transactions |
| Num_BillPay | int | Total amount of successful bill payment transactions |
| Num_MerchantPay | int | Total amount of successful merchant payment transactions |
| Num_SalaryPayments | int | Total amount of successful salary payment transactions |
| Amnt_CashIN | numeric(38,2) | Total revenues from cash-in (end user fees for cash-in transactions )|
| Amnt_CashOUT | numeric(38,2) | Total revenues from cash-out (end user fees for cash-out transactions) |
| Amnt_P2P | numeric(38,2) | Total revenues from P2P (end user fees for P2P transactions )|
| Amnt_P2pNoReg | numeric(38,2) | Total revenues from TNO (end user fees for transfer to non Orange transactions) |
| Amnt_Airtime | numeric(38,2) | Total revenues from top up (end user fees for top-up transactions ) |
| Amnt_BillPay | numeric(38,2) | Total revenues from bill payment  (end user fees for bill payment transactions ) |
| Amnt_MerchantPay | numeric(38,2) | Total revenues from merchant payment (end user fees for merchant payment transactions ) |
| Amnt_SalaryPayments | numeric(38,2) | Total revenues from salary payment transactions (end user fees for salary payment transactions ) |
| Rev_CashOut | numeric(38,2) | Total revenues from Cash Out  (end user fees for Cash out transactions ) |
| Rev_P2P | numeric(38,2) | Total revenues from P2P  (end user fees for P2P transactions ) |
| Rev_BillPay | numeric(38,2) | Total revenues from Bill Payment  (end user fees for payment of bills [insurance, food delivery,...]  transactions ) |
| Rev_Merchant Pay | numeric(38,2) | Total revenues from Merchant Payment  (end user fees for payment of goods and services to merchants transactions )|
| CommissionPaid_CashIN | numeric(38,2) | Commissions paid to distributors on customer Cash-in transactions |
| CommissionPaid_CashOUT | numeric(38,2) | Commissions paid to distributors on customer Cash-out transactions |
| Rev_SalaryPay | numeric(38,2) | Total revenues from salary payment transactions (end user fees for salary payment transactions ) |
| Num_SubscriberBundles | int | Total transactions number of bundle purchases done by Subscribers (using #144) for themselves or others |
| Num_AgentBundles | int | Total transactions number of bundle purchases done by Agents (using #154) for themselves or others |
| Amnt_SubscriberBundles | numeric(38,2) | Total transactions amount of successful bundle purchases done by Subscribers (using #144) for themselves or others |
| Amnt_AgentBuyBundles | numeric(38,2) | Total transactions amount of successful bundle purchases done by Agents (using #154) for themselves or others |
| Rev_SubscriberBuyBundles | numeric(38,2) | Total revenues from successful bundle purchases done by Subscribers (using #144) for themselves or others |
| Rev_AgentsBuyBundles | numeric(38,2) | Total revenues from amount of successful bundle purchases done by Agents (using #154) for themselves or others |
| Num_BetIN | int | Total number of successful online betting "IN" transactions (end user payments) |
| Num_BetOUT | int | Total number of successful online betting "OUT" transactions (end user reimbursements) |
| Amnt_BettingIN | numeric(38,2) | Total amount of successful online betting "IN" transactions (payments) |
| Amnt_BettingOUT | numeric(38,2) | Total amount of successful online betting "OUT" transactions (end user reimbursements) |
| Rev_BettingIN | numeric(38,2) | Total revenues of online betting "IN" transactions (payments) (end user fee for online betting "IN" transactions aka payments from customer to betting company) |
| Rev_BettingOut | numeric(38,2) | Total revenues of online betting "OUT" transactions (reimbursements) (end user fee for online betting "OUT" transactions aka reimbursements from betting company to customer) |
| Num_LEC | int | Total number of successful LEC transactions |
| Amnt_LEC | numeric(38,2) | Total amount of successful LEC transactions |
| Rev_LEC | numeric(38,2) | Total revenues of LEC transactions (end user fee from LEC transactions ) |
| Num_DSTv | int | Total number of successful TV transactions |
| Amnt_DSTv | numeric(38,2) | Total amount of successful TV transactions |
| Rev_DSTv | numeric(38,2) | Total revenues of TV transactions (end user fee from TV transactions ) |
| Num_P2G | int | Total number of successful Person-to-Goverment transactions |
| Amnt_P2G | numeric(38,2) | Total amount of successful Person-to-Goverment transactions |
| Rev_P2G | numeric(38,2) | Total revenues of Person-to-Goverment transactions (end user fee from Person-to-Goverment transactions )  |
| Num_B2W | int | Total number of successful Bank-to-Wallet transactions |
| Num_W2B | int | Total number of successful Wallet-to-Bank transactions |
| Amnt_B2W | numeric(38,2) | Total amount of successful Bank-to-Wallet transactions |
| Amnt_W2B | numeric(38,2) | Total amount of successful Wallet-to-Bank transactions |
| Rev_B2W | numeric(38,2) | Total revenue of successful Bank-to-Wallet transactions |
| Rev_W2B | numeric(38,2) | Total revenue of successful Wallet-to-Bank transactions |
| Num_IRTOUT | int | Total number of successful outbound International Remitance transactions |
| Num_IRTIN | int | Total number of successful inbound International Remitance transactions |
| Amnt_IRTOUT | numeric(38,2) | Total amount of successful IRT (intra régional transfert) OUT transactions |
| Amnt_IRTIN | numeric(38,2) | Total amount of successful IRT (intra régional transfert) IN transactions |
| Rev_IRTOUT | numeric(38,2) | Total revenues from "IRT OUT" transactions (end user fees for IRT (intra régional transfert) OUT transactions) |
| Rev_IRTIN | numeric(38,2) | Total revenues from "IRT IN" transactions (end user fees for IRT (intra régional transfert) IN transactions) |
| Num_OrangeEnergy | int | Total number of successful Orange Energy transactions |
| Amnt_OrangeEnergy | numeric(38,2) | Total amount of successful Orange Energy transactions |
| Rev_OrangeEnergy | numeric(38,2) | Total revenues from Orange Energy transactions |
---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

