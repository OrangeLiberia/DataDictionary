#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [BI](../index.md) > [Tables](Tables.md) > fwk.CountryCodes

# ![Tables](../../../../Images/Table32.png) [fwk].[CountryCodes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| ID | int | 4 | NOT NULL | 1 - 1 |
| DialingCode | varchar(10) | 10 | NULL allowed |  |
| CountryName | varchar(100) | 100 | NULL allowed |  |


---

## <a name="#uses"></a>Uses

* [fwk]


---

## <a name="#usedby"></a>Used By

* [[fwk].[fnc_GetCountryName]](../Programmability/Functions/Scalar-valued_Functions/fnc_GetCountryName.md)


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

