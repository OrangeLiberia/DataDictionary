#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.OMmonthlyledger

# ![Tables](../../../../Images/Table32.png) [dbo].[OMmonthlyledger]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__OMmonthl__3214EC277AA6D067: ID](../../../../Images/pkcluster.png)](#indexes) | ID | bigint | 8 | NOT NULL | 1 - 1 |
|  | Subscriber_lifetime | numeric(19,2) | 9 | NULL allowed |  |
|  | Refdate | date | 3 | NULL allowed |  |
|  | CREATION_DATE | datetime | 8 | NULL allowed |  |
|  | SERVICE_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | DESIGNATION | varchar(100) | 100 | NULL allowed |  |
|  | DOMAIN_CODE | varchar(100) | 100 | NULL allowed |  |
|  | TAG | varchar(100) | 100 | NULL allowed |  |
|  | TRANSACTION_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | Week | int | 4 | NULL allowed |  |
|  | FRIST_OF_MONTH | date | 3 | NULL allowed |  |
|  | LAST_OF_MONTH | date | 3 | NULL allowed |  |
|  | ACCOUNT_LEVEL | varchar(100) | 100 | NULL allowed |  |
|  | GRADE | varchar(100) | 100 | NULL allowed |  |
|  | STATE | varchar(100) | 100 | NULL allowed |  |
|  | TOTAL_AMOUNT | numeric(19,2) | 9 | NULL allowed |  |
|  | N_TRANSACTIONS | numeric(19,2) | 9 | NULL allowed |  |
|  | TRANSACTION_TAG | varchar(100) | 100 | NULL allowed |  |
|  | CurrencyType | varchar(3) | 3 | NULL allowed |  |
|  | MSISDN | varchar(100) | 100 | NULL allowed |  |
|  | NAME | varchar(100) | 100 | NULL allowed |  |
|  | Commisisons | numeric(19,2) | 9 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__OMmonthl__3214EC277AA6D067: ID](../../../../Images/pkcluster.png)](#indexes) | PK__OMmonthl__3214EC277AA6D067 | ID | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

