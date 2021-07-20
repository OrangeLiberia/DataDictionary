#### 

# # Quick Description

# # TIMMBI\\BI Documentation (192.168.19.120\BI)
|Database|Description|Comment|
--- | --- | ---
|BI|IN Transactions (SC, VAS, etc) IN CDRs, MSC CDRs, MSC Data CDRs, Revenue, BI processed data for reporting, ARPUs etc||
|RepositoryXXXXX|Data details from the multiple NEs (msc, in, crm, ...) ||
|TIMM_Reports|Data summarized for new BI reports after V9||
|External|BI configuration tables||

# # TIMMMEDIBLNG\\MEDIBLNG Documentation (192.168.19.11\MEDIBLNG)
|Database|Description|Comment|
--- | --- | ---
|TIMM_COMUNS|CRM and roaming configuration tables (Operators, etc)|(replication from TIMMCRMPROV)|
|TIMM_CRM|CRM data (services, clientes, accounts, SIM REG, KYC, KYA  NIR etc)|(replication from TIMMCRMPROV)|
|TIMM_PRICING|Invoicing configuration tables (profiles, pricing, etc)|(replication from TIMMCRMPROV)|
|TIMM_EXTRAS|Data summarized for old MEDI reports ||
|TIMM_Reports|Data summarized for new MEDI reports after V9 ||
|TIMM_DMP_TAP|Roaming xDR repository (TAP's & NRTRDE's) ||
|TIMM_ROAMING|Configuration roaming tables (agreements, etc) ||
|TIMM_INTERCONNECT_XXXXX|Monthly interconnect processed data ||
|DW_OrangeMoney|Orange Money Datawarehouse data|(DHW imported data)|


# # TIMMPRVCRM\\PRVCRM Documentation (192.168.19.30\CRMPROV)
|Database|Description|Comment|
--- | --- | ---
|TIMM_COMUNS|CRM and roaming configuration tables (Operators, etc)||
|TIMM_CRM|CRM data (services, clientes, accounts, SIM REG, KYC, KYA  NIR etc)||
|TIMM_PRICING|Invoicing configuration tables (profiles, pricing, etc)||
|TIMM_CRM_SNAPSHOT|Snap monthly snapshot of selection of tables of database TIMM CRM||
|TIMM_EXTRAS|Data summarized for old CRM reports, HLR recon, clean up numbers, sim activations||
|TIMM_Reports|Data summarized for new CRM reports after V9||
|TIMM_HIST|CRM history data (interactions, sim swap, sim reg information changed)||




###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, July 12, 2021 6:27:35 PM

