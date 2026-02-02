#### 

[Project](../../../../index.md) > [192.168.19.40\\CRMPROV](../../../index.md) > [User databases](../../index.md) > [TIMM_CRM](../index.md) > [Views](Views.md) > dbo.TbccServicos_GSM

# ![Views](../../../../Images/View32.png) [dbo].[TbccServicos_GSM]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| id | int | 4 | 0 - 0 |
| imei | numeric(19,0) | 9 |  |
| imsi | varchar(15) | 15 |  |
| iccid | varchar(18) | 18 |  |
| mainkey | varchar(50) | 50 |  |
| entidade | numeric(18,0) | 9 |  |
| status | tinyint | 1 |  |
| pin1 | varchar(8) | 8 |  |
| pin2 | varchar(8) | 8 |  |
| puk1 | varchar(8) | 8 |  |
| puk2 | varchar(8) | 8 |  |
| ki | nvarchar(400) | 800 |  |
| lastuserid | int | 4 |  |
| created_at | datetime | 8 |  |
| updated_at | datetime | 8 |  |
| TipoCartaoID | int | 4 |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

