#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.TransactionMSISDNTrackingReport

# ![Tables](../../../../Images/Table32.png) [dbo].[TransactionMSISDNTrackingReport]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ReportType | varchar(32) | 32 | NOT NULL |
| MSISDN | varchar(10) | 10 | NOT NULL |
| Currency | varchar(4) | 4 | NOT NULL |
| TransactionList | varchar(256) | 256 | NULL allowed |
| MinAmount | money | 8 | NULL allowed |
| MaxAmount | money | 8 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

