#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_COMUNS](../index.md) > [Tables](Tables.md) > dbo.Tcom_WNP_MobileOperators

# ![Tables](../../../../Images/Table32.png) [dbo].[Tcom_WNP_MobileOperators]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Tcom_WNP_MobileOperators: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | IDParentOperator | int | 4 | NULL allowed |
|  | OperatorName | varchar(150) | 150 | NULL allowed |
|  | NetworkName | varchar(150) | 150 | NULL allowed |
|  | HandsetCode | varchar(50) | 50 | NULL allowed |
|  | ISO-3166-1_alpha-2 | varchar(2) | 2 | NULL allowed |
|  | ISO-3166-1_alpha-3 | varchar(3) | 3 | NULL allowed |
|  | MCC | varchar(3) | 3 | NULL allowed |
|  | MNC | varchar(3) | 3 | NULL allowed |
|  | Homeoperator | tinyint | 1 | NULL allowed |
|  | PLMNID | varchar(10) | 10 | NULL allowed |
|  | Status | int | 4 | NULL allowed |
|  | LastuserID | int | 4 | NULL allowed |
|  | LastUpdate | datetime | 8 | NULL allowed |
|  | OperatorType | nvarchar(50) | 100 | NULL allowed |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

