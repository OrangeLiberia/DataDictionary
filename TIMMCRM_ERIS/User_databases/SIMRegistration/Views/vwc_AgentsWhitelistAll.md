#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Views](Views.md) > dbo.vwc_AgentsWhitelistAll

# ![Views](../../../../Images/View32.png) [dbo].[vwc_AgentsWhitelistAll]

---

## <a name="#description"></a>MS_Description

View all the Agent Whitelist 

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Created | 10:28:37 AM Thursday, April 11, 2019 |
| Last Modified | 10:28:37 AM Thursday, April 11, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | int | 4 |
| MSISDN | varchar(20) | 20 |
| IMEI | varchar(20) | 20 |
| ICCID | varchar(20) | 20 |
| TIMM_SIM_MSISDN | varchar(20) | 20 |
| TIMM_SIM_ICCID | varchar(20) | 20 |
| TIMM_Status | int | 4 |
| AgentNickName | varchar(50) | 50 |
| AgentName | varchar(100) | 100 |
| AgentDescription | varchar(200) | 200 |
| DateInsert | datetime | 8 |
| Active | bit | 1 |
| TIMM_ServicoID | numeric(18,0) | 9 |
| Dealer | varchar(128) | 128 |
| Channel | varchar(128) | 128 |
| SubChannel | varchar(128) | 128 |
| Location | varchar(128) | 128 |
| Deleted | bit | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
create view [dbo].[vwc_AgentsWhitelistAll]
AS
	SELECT [ID], [MSISDN], [IMEI], [ICCID], [TIMM_SIM_MSISDN], [TIMM_SIM_ICCID], [TIMM_Status], [AgentNickName], [AgentName], [AgentDescription], [DateInsert], [Active], [TIMM_ServicoID], [Dealer], [Channel], [SubChannel], [Location], CONVERT(bit,0) Deleted
	from [dbo].[AgentsWhitelist] with (nolock)
	union 
	SELECT [ID], [MSISDN], [IMEI], [ICCID], [TIMM_SIM_MSISDN], [TIMM_SIM_ICCID], [TIMM_Status], [AgentNickName], [AgentName], [AgentDescription], [DateInsert], [Active], [TIMM_ServicoID], [Dealer], [Channel], [SubChannel], [Location], CONVERT(bit,0) Deleted
	from [AgentsWhitelistHist] with (nolock)
GO
EXEC sp_addextendedproperty N'MS_Description', N'View all the Agent Whitelist ', 'SCHEMA', N'dbo', 'VIEW', N'vwc_AgentsWhitelistAll', NULL, NULL
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[AgentsWhitelist]](../Tables/AgentsWhitelist.md)
* [[dbo].[AgentsWhitelistHist]](../Tables/AgentsWhitelistHist.md)


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

