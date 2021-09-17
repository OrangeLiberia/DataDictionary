#### 

[Project](../../../../index.md) > [192.168.19.40\\ERIS](../../../index.md) > [User databases](../../index.md) > [SIMRegistration](../index.md) > [Tables](Tables.md) > dbo.AgentsWhitelist

# ![Tables](../../../../Images/Table32.png) [dbo].[AgentsWhitelist]

---

## <a name="#description"></a>MS_Description

SIM Registration Whitelist

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity | Default | Description |
|---|---|---|---|---|---|---|---|
| [![Indexes UNQ_AgentsWhitelist_ID](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |  |  |
| [![Cluster Primary Key PK_AgentsWhitelist: MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes) | MSISDN | varchar(20) | 20 | NOT NULL |  |  | _Agent MSISDN_ |
| [![Cluster Primary Key PK_AgentsWhitelist: MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes)[![Indexes UNQ_AgentsWhitelist_ICCID](../../../../Images/Index.png)](#indexes) | IMEI | varchar(20) | 20 | NOT NULL |  |  | _Agent Device Identification_ |
| [![Indexes UNQ_AgentsWhitelist_ICCID](../../../../Images/Index.png)](#indexes) | ICCID | varchar(20) | 20 | NOT NULL |  |  | _Agent SIM Identification_ |
|  | TIMM_SIM_MSISDN | varchar(20) | 20 | NULL allowed |  |  | _MSISDN on the CRM_ |
|  | TIMM_SIM_ICCID | varchar(20) | 20 | NULL allowed |  |  | _ICCID on the CRM_ |
|  | TIMM_Status | int | 4 | NULL allowed |  |  | _Status of the MSISDN on the CRM_ |
|  | AgentNickName | varchar(50) | 50 | NULL allowed |  |  | _Agent nickname_ |
|  | AgentName | varchar(100) | 100 | NULL allowed |  |  | _Agent name_ |
|  | AgentDescription | varchar(200) | 200 | NULL allowed |  |  | _Agent description_ |
|  | DateInsert | datetime | 8 | NOT NULL |  | (getdate()) | _Datetime of creation_ |
|  | Active | bit | 1 | NULL allowed |  | ((0)) | _Status of the Agent whitelist ( 0 - disabled, 1- active)_ |
|  | TIMM_ServicoID | numeric(18,0) | 9 | NULL allowed |  |  | _CRM ServiceID_ |
|  | Dealer | varchar(128) | 128 | NULL allowed |  |  | _Agent Classification_ |
|  | Channel | varchar(128) | 128 | NULL allowed |  | ('Unknown') | _Agent Channel_ |
|  | SubChannel | varchar(128) | 128 | NULL allowed |  |  | _Agent Subchannel_ |
|  | Location | varchar(128) | 128 | NULL allowed |  |  | _Agent Location_ |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_AgentsWhitelist: MSISDN\IMEI](../../../../Images/pkcluster.png)](#indexes) | PK_AgentsWhitelist | MSISDN, IMEI | YES |
|  | UNQ_AgentsWhitelist_ICCID | ICCID, IMEI | YES |
|  | UNQ_AgentsWhitelist_ID | ID | YES |


---

###### Author:  WDAGUtilityAccount

###### Copyright 2021 - All Rights Reserved

###### Created: Thursday, September 16, 2021 10:19:43 PM

