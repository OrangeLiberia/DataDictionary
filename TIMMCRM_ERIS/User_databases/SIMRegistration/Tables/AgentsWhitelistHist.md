#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.AgentsWhitelistHist

# ![Tables](../../../../Images/Table32.png) [dbo].[AgentsWhitelistHist]

---

## <a name="#description"></a>MS_Description

SIM Registration Whitelist history

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Default | Description |
|---|---|---|---|---|---|
| ID | int | 4 | NOT NULL |  | _ID_ |
| MSISDN | varchar(20) | 20 | NOT NULL |  | _Agent MSISDN_ |
| IMEI | varchar(20) | 20 | NOT NULL |  | _Agent Device Identification_ |
| ICCID | varchar(20) | 20 | NOT NULL |  | _Agent SIM Identification_ |
| TIMM_SIM_MSISDN | varchar(20) | 20 | NULL allowed |  | _MSISDN on the CRM_ |
| TIMM_SIM_ICCID | varchar(20) | 20 | NULL allowed |  | _ICCID on the CRM_ |
| TIMM_Status | int | 4 | NULL allowed |  | _Status of the MSISDN on the CRM_ |
| AgentNickName | varchar(50) | 50 | NULL allowed |  | _Agent nickname_ |
| AgentName | varchar(100) | 100 | NULL allowed |  | _Agent name_ |
| AgentDescription | varchar(200) | 200 | NULL allowed |  | _Agent description_ |
| DateInsert | datetime | 8 | NOT NULL |  | _Datetime of creation_ |
| Active | bit | 1 | NOT NULL |  | _Status of the Agent whitelist (0 - disabled, 1- active)_ |
| TIMM_ServicoID | numeric(18,0) | 9 | NULL allowed |  | _CRM Service ID_ |
| Dealer | varchar(128) | 128 | NULL allowed |  | _Agent Classification_ |
| Channel | varchar(128) | 128 | NULL allowed |  | _Agent Channel_ |
| SubChannel | varchar(128) | 128 | NULL allowed |  | _Agent SubChannel_ |
| Location | varchar(128) | 128 | NULL allowed |  | _Agent Location_ |
| DateDelete | datetime | 8 | NOT NULL | (getdate()) | _Datetime of deletion_ |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

