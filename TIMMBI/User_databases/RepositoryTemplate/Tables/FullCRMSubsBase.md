#### 

[Project](../../../../index.md) > [192.168.19.120\\BI](../../../index.md) > [User databases](../../index.md) > [RepositoryTemplate](../index.md) > [Tables](Tables.md) > crm.FullCRMSubsBase

# ![Tables](../../../../Images/Table32.png) [crm].[FullCRMSubsBase]

---

## <a name="#description"></a>MS_Description

Subscriber Base for the Month

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Description |
|---|---|---|---|---|---|
|  | ServicoID | numeric(18,0) | 9 | NOT NULL | _Unique Identifier of the Service ID_ |
|  | ContaID | numeric(18,0) | 9 | NULL allowed | _Unique Identifier for the Client Account_ |
|  | ClienteID | numeric(18,0) | 9 | NULL allowed | _Unique Identifier for the Client_ |
| [![Indexes IX_FullCRMSubsBase](../../../../Images/Index.png)](#indexes) | MSISDN9 | varchar(51) | 51 | NOT NULL | _9 Digit MSISDN_ |
|  | MSISDN8 | varchar(50) | 50 | NOT NULL | _8 Digit MSISDN_ |
|  | TipoCartaoID | int | 4 | NULL allowed | _Type of SIM Card_ |
|  | ICCID | varchar(18) | 18 | NULL allowed | _ICCID_ |
|  | IMSI | numeric(19,0) | 9 | NULL allowed | _IMSI_ |
|  | PreActDate | datetime | 8 | NULL allowed |  |
|  | PrePos | varchar(3) | 3 | NOT NULL |  |
|  | ClientName | varchar(200) | 200 | NULL allowed | _Client name_ |
|  | AccountName | varchar(200) | 200 | NULL allowed | _Account name_ |
|  | SubsName | varchar(200) | 200 | NULL allowed | _Subscriber name_ |
|  | IDCard | varchar(20) | 20 | NULL allowed | _Identification document number_ |
|  | IDCardType | varchar(100) | 100 | NOT NULL | _Identification document type_ |
|  | BirthDate | datetime | 8 | NOT NULL | _Birth date_ |
|  | Gender | varchar(50) | 50 | NULL allowed | _Gender_ |
|  | Address | varchar(200) | 200 | NULL allowed | _Address_ |
|  | IDCountry | int | 4 | NULL allowed | _Id for the country_ |
|  | CountryName | varchar(50) | 50 | NULL allowed | _Country name_ |
|  | Nacionality | varchar(150) | 150 | NULL allowed | _Nationality_ |
|  | FakeReg | tinyint | 1 | NULL allowed | _Migration flag_ |
|  | DataValid | int | 4 | NULL allowed |  |
|  | NPics | int | 4 | NOT NULL |  |
|  | SimRegApp | varchar(10) | 10 | NULL allowed |  |
|  | DataService | tinyint | 1 | NULL allowed |  |
|  | Corporate | bit | 1 | NULL allowed |  |
|  | Protected | tinyint | 1 | NULL allowed |  |
|  | TIMMRegistered | tinyint | 1 | NOT NULL |  |
|  | SIMRegistered | tinyint | 1 | NULL allowed |  |
|  | CRMLastStatusUpdate | datetime | 8 | NULL allowed |  |
|  | StatusChangedDuringTF | bit | 1 | NOT NULL |  |
|  | BIFirstActivity | datetime | 8 | NULL allowed | _First network activity _ |
|  | BILastActivity | datetime | 8 | NULL allowed | _Last network activity_ |
|  | BIActivityBeforeTF | bit | 1 | NULL allowed |  |
|  | BIActivityDuringTF | bit | 1 | NULL allowed |  |
|  | LastIMEI | varchar(20) | 20 | NULL allowed |  |
|  | LastCellID | int | 4 | NULL allowed | _Last CELL ID_ |
|  | Data1 | varchar(max) | max | NULL allowed |  |
|  | Data2 | varchar(max) | max | NULL allowed |  |
|  | Registered | tinyint | 1 | NULL allowed | _Subscriber Registration flag_ |
|  | ValidGSM | tinyint | 1 | NULL allowed | _Subscriber GSM validation flag_ |
|  | DescStatusGSM | varchar(200) | 200 | NULL allowed | _Description of the GSM validation flag_ |
|  | ValidOM | tinyint | 1 | NULL allowed | _Subscriber Orange Money validation flag_ |
|  | DescStatusOM | varchar(200) | 200 | NULL allowed | _Description of the Orange Money validation flag_ |
|  | DateValidationStatus | datetime | 8 | NULL allowed | _Date of the last validation_ |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns |
|---|---|
| IX_FullCRMSubsBase | MSISDN9 |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 3:15:24 PM

