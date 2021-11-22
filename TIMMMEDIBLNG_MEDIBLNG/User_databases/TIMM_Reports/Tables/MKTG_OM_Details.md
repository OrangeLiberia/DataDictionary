#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.MKTG_OM_Details

# ![Tables](../../../../Images/Table32.png) [dbo].[MKTG_OM_Details]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 0 |
| Created | 1:35:10 AM Monday, September 20, 2021 |
| Last Modified | 1:35:10 AM Monday, September 20, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__MKTG_OM___3214EC27D9FDAA92: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | Refmonth | varchar(8) | 8 | NULL allowed |  |
|  | Week | int | 4 | NULL allowed |  |
|  | msisdn | varchar(10) | 10 | NULL allowed |  |
|  | TAG | varchar(100) | 100 | NULL allowed |  |
|  | Total_transactions | int | 4 | NULL allowed |  |
|  | Amount | numeric(17,2) | 9 | NULL allowed |  |
|  | Weekly_lifetime | int | 4 | NULL allowed |  |
|  | currencytype | varchar(3) | 3 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

