#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Reports](../index.md) > [Tables](Tables.md) > dbo.destination

# ![Tables](../../../../Images/Table32.png) [dbo].[destination]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Heap | YES |
| Row Count (~) | 60529 |
| Created | 4:49:38 PM Wednesday, May 19, 2021 |
| Last Modified | 4:49:38 PM Wednesday, May 19, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ID | int | 4 | NOT NULL |
| IDCNS | int | 4 | NOT NULL |
| cns | varchar(20) | 20 | NOT NULL |
| IDParent | int | 4 | NULL allowed |
| IDCountryCode | smallint | 2 | NOT NULL |
| IDRegistrar | int | 4 | NOT NULL |
| IDType | varchar(6) | 6 | NOT NULL |
| IDLocation | int | 4 | NOT NULL |
| CountryCode | varchar(5) | 5 | NULL allowed |
| Destination | varchar(50) | 50 | NULL allowed |
| RegistrarDesc | varchar(200) | 200 | NULL allowed |
| LocationDesc | varchar(100) | 100 | NULL allowed |
| IDContinent | smallint | 2 | NULL allowed |
| ContinentDesc | varchar(max) | max | NULL allowed |


---

## <a name="#permissions"></a>Permissions

| Type | Action | Owning Principal |
|---|---|---|
| Grant | SELECT | olib_bu_sales |
| Grant | VIEW DEFINITION | olib_bu_sales |
| Grant | SELECT | olib_bu_orangemoney |
| Grant | VIEW DEFINITION | olib_bu_orangemoney |
| Grant | SELECT | olib_bu_mis_add |
| Grant | VIEW DEFINITION | olib_bu_mis_add |
| Grant | SELECT | olib_bu_finance |
| Grant | VIEW DEFINITION | olib_bu_finance |
| Grant | SELECT | olib_bu_marketing |
| Grant | VIEW DEFINITION | olib_bu_marketing |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

