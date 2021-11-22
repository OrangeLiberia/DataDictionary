#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.FDD_Numbers

# ![Tables](../../../../Images/Table32.png) [dbo].[FDD_Numbers]

---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| day | date | 3 | NOT NULL |
| MSISDN | varchar(50) | 50 | NOT NULL |
| Type | nvarchar(50) | 100 | NOT NULL |
| IMEI | int | 4 | NOT NULL |
| device_type | nvarchar(50) | 100 | NOT NULL |
| device_brand | nvarchar(50) | 100 | NOT NULL |
| device_model | nvarchar(50) | 100 | NOT NULL |
| device_tekradio | nvarchar(50) | 100 | NULL allowed |
| APN | nvarchar(50) | 100 | NOT NULL |
| offer | nvarchar(50) | 100 | NOT NULL |
| total_volume_bytes | float | 8 | NOT NULL |
| Usage_MB | float | 8 | NOT NULL |
| volume_rat_3G_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_rat_2G_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_rat_LTE_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Unknown_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Web_bytes | float | 8 | NOT NULL |
| volume_appli_P2P_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Download_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_News_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Mail_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_DB_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Others_bytes | int | 4 | NOT NULL |
| volume_appli_Control_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Games_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Streaming_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_Chat_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_VoIP_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_MailOrange_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_VPN_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_ICMP_DNS_bytes | float | 8 | NOT NULL |
| volume_appli_MMS_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_MobileTV_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_appli_OrangePortal_bytes | nvarchar(50) | 100 | NOT NULL |
| volume_outbound_roaming_bytes | nvarchar(50) | 100 | NOT NULL |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

