#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Views](Views.md) > dbo.vwt_BundlesV9PerMSISDN_NEW

# ![Views](../../../../Images/View32.png) [dbo].[vwt_BundlesV9PerMSISDN_NEW]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:04:57 PM Friday, November 20, 2020 |
| Last Modified | 3:04:57 PM Friday, November 20, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Day | char(10) | 10 |
| MSISDN | varchar(9) | 9 |
| BundleID | int | 4 |
| Bundle | varchar(100) | 100 |
| ActivationsUSSD | int | 4 |
| FeeUSSD | decimal(38,6) | 17 |
| ActivationsOM | int | 4 |
| FeeOM | numeric(38,17) | 17 |
| Data Volume | bigint | 8 |
| ONNETNumCalls | bigint | 8 |
| ONNETSeconds | bigint | 8 |
| ONNETNumSMS | bigint | 8 |
| OFFNETNumCalls | bigint | 8 |
| OFFNETSeconds | bigint | 8 |
| OFFNETNumSMS | bigint | 8 |
| INTNumCalls | bigint | 8 |
| INTSeconds | bigint | 8 |
| INTNumSMS | bigint | 8 |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | SELECT | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | SELECT | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | SELECT | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | SELECT | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | SELECT | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

## <a name="#uses"></a>Uses

* [[dbo].[tbc_BundleID]](../Tables/tbc_BundleID.md)
* [[dbo].[tbc_V9CampaignsBundleDR]](../Tables/tbc_V9CampaignsBundleDR.md)
* [[dbo].[tbc_V9CampaignsSubAct]](../Tables/tbc_V9CampaignsSubAct.md)
* [[DW_OrangeMoney].[dbo].[Transactions]](../../DW_OrangeMoney/Tables/Transactions.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

