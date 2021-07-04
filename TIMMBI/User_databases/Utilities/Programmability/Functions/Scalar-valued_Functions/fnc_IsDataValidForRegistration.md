#### 

[Project](../../../../../../index.md) > [TIMMBI\\BI](../../../../../index.md) > [User databases](../../../../index.md) > [Utilities](../../../index.md) > [Programmability](../../index.md) > [Functions](../index.md) > [Scalar-valued Functions](Scalar-valued_Functions.md) > simreg.fnc_IsDataValidForRegistration

# ![Scalar-valued Functions](../../../../../../Images/Function_Scalar32.png) [simreg].[fnc_IsDataValidForRegistration]

---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @FullName | varchar(150) | 150 |
| @Gender | varchar(20) | 20 |
| @BirthDate | datetime | 8 |
| @Address | varchar(200) | 200 |
| @IDCard | varchar(20) | 20 |
| @IDCardType | varchar(50) | 50 |
| @Corporate | bit | 1 |


---

## <a name="#uses"></a>Uses

* [[simreg].[fnc_IsAddressValid]](fnc_IsAddressValid.md)
* [[simreg].[fnc_IsNameValid]](fnc_IsNameValid.md)
* [simreg](../../../Security/Schemas/simreg.md)


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

