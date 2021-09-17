#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.vwc_TimmCustomerProfile

# ![Views](../../../../Images/View32.png) [dbo].[vwc_TimmCustomerProfile]

---

## <a name="#description"></a>MS_Description

View Customer Profile on the CRM

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| ANSI Nulls On | YES |
| Created | 3:40:10 AM Tuesday, April 19, 2016 |
| Last Modified | 5:06:46 PM Saturday, August 15, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| MSISDN | varchar(50) | 50 |
| ServicoID | numeric(18,0) | 9 |
| ProfilePlanID | int | 4 |
| MMProfilePlanID | int | 4 |
| Status | tinyint | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql


CREATE view [dbo].[vwc_TimmCustomerProfile] as 
	select	S.MSISDN, S.ServicoID, S.ProfilePlanID, PP.MMProfilePlanID, S.Status 
	from	[TIMM.CRM].TIMM_CRM.dbo.TIMM_Servicos S 
			inner join [TIMM.CRM].TIMM_PRICING.dbo.tbccProfilePlans PP on S.ProfilePlanID = PP.ProfilePlanID 
	where	S.Status != 9 and isnull(S.MSISDN,'') != ''
GO
EXEC sp_addextendedproperty N'MS_Description', N'View Customer Profile on the CRM', 'SCHEMA', N'dbo', 'VIEW', N'vwc_TimmCustomerProfile', NULL, NULL
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[sps_SIMRegistrationAttempt]](../Programmability/Stored_Procedures/sps_SIMRegistrationAttempt.md)


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

