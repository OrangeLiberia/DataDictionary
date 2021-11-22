#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [DW_OrangeMoney](../index.md) > [Tables](Tables.md) > dbo.ReportLevel

# ![Tables](../../../../Images/Table32.png) [dbo].[ReportLevel]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Primary Key PK_tbc_V9Campaigns: ID\ReferenceDay](../../../../Images/pk.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
| [![Primary Key PK_tbc_V9Campaigns: ID\ReferenceDay](../../../../Images/pk.png)](#indexes) | ReferenceDay | smalldatetime | 4 | NOT NULL |  |
|  | CurrentChangeDate | datetime | 8 | NULL allowed |  |
|  | Currency | varchar(6) | 6 | NULL allowed |  |
|  | MSISDN | varchar(15) | 15 | NULL allowed |  |
|  | MSISDN8 | varchar(15) | 15 | NULL allowed |  |
|  | Current_USER_GRADE_NAME | varchar(40) | 40 | NULL allowed |  |
|  | OMLevel | int | 4 | NULL allowed |  |
|  | CRMLevel | int | 4 | NULL allowed |  |
|  | CRMGSMValidation | int | 4 | NULL allowed |  |
|  | CRMOMValidation | int | 4 | NULL allowed |  |
|  | Status | tinyint | 1 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Primary Key PK_tbc_V9Campaigns: ID\ReferenceDay](../../../../Images/pk.png)](#indexes) | PK_tbc_V9Campaigns | ID, ReferenceDay | YES |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

