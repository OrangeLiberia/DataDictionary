#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_Report](../index.md) > [Tables](Tables.md) > dbo.Compliance_ctc_report

# ![Tables](../../../../Images/Table32.png) [dbo].[Compliance_ctc_report]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 6119 |
| Created | 9:36:52 AM Monday, June 21, 2021 |
| Last Modified | 9:36:52 AM Monday, June 21, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK__Complian__3214EC278A979595: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
|  | REFDATE | date | 3 | NULL allowed |  |
|  | SURNAME_NAME_OF_ORGANISATION | varchar(100) | 100 | NULL allowed |  |
|  | FIRST_NAME | varchar(100) | 100 | NULL allowed |  |
|  | MIDDLE_NAME | varchar(100) | 100 | NULL allowed |  |
|  | BANK_NAME | varchar(100) | 100 | NULL allowed |  |
|  | INSTUTUTION_CODE | varchar(100) | 100 | NULL allowed |  |
|  | BRANCH | varchar(100) | 100 | NULL allowed |  |
|  | REPORT_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | CUSTOMER_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | NATIONALITY | varchar(100) | 100 | NULL allowed |  |
|  | DATE_OF_INCORPORATION_BIRTH | varchar(100) | 100 | NULL allowed |  |
|  | OCCUPATION_LINE_OF_BUSINESS | varchar(100) | 100 | NULL allowed |  |
|  | TYPE_OF_IDENTIFICATION | varchar(100) | 100 | NULL allowed |  |
|  | REGISTRATION_NO | varchar(100) | 100 | NULL allowed |  |
|  | IDENTIFICATION_NO | varchar(100) | 100 | NULL allowed |  |
|  | DATE_OF_ISSUE | date | 3 | NULL allowed |  |
|  | PLACE_OF_ISSUE | varchar(100) | 100 | NULL allowed |  |
|  | ISSUING_AUTHORITY | varchar(100) | 100 | NULL allowed |  |
|  | RESIDENTIAL_ADDRESS | varchar(100) | 100 | NULL allowed |  |
|  | POSTAL_ADDRESS | varchar(100) | 100 | NULL allowed |  |
|  | TOWN_CITY | varchar(100) | 100 | NULL allowed |  |
|  | REGION | varchar(100) | 100 | NULL allowed |  |
|  | TEL | varchar(100) | 100 | NULL allowed |  |
|  | EMAIL | varchar(100) | 100 | NULL allowed |  |
|  | ACCOUNT_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | ACCOUNT_NO | varchar(100) | 100 | NULL allowed |  |
|  | ACCOUNT_STATUS | varchar(100) | 100 | NULL allowed |  |
|  | DATE_OPENED | varchar(100) | 100 | NULL allowed |  |
|  | LINK_CONNECTED_ACCOUNTS | varchar(100) | 100 | NULL allowed |  |
|  | TRANSACTION_NO | varchar(100) | 100 | NULL allowed |  |
|  | TRANSACTION_DATE | date | 3 | NULL allowed |  |
|  | TRANSACTION_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | DR_CR | varchar(100) | 100 | NULL allowed |  |
|  | TRANSACTION_PARTICULARS | varchar(100) | 100 | NULL allowed |  |
|  | CURRENCY_TYPE | varchar(100) | 100 | NULL allowed |  |
|  | AMOUNT_FOREIGN_CURRENCY | varchar(100) | 100 | NULL allowed |  |
|  | EXCHANGE_RATE | varchar(100) | 100 | NULL allowed |  |
|  | AMOUNT_LOCAL_CURRENCY | varchar(100) | 100 | NULL allowed |  |
|  | TOTAL_TRANSACTION_AMOUNT | varchar(100) | 100 | NULL allowed |  |
|  | PURPOSE_OF_TRANSACTION | varchar(100) | 100 | NULL allowed |  |
|  | SOURCE_ORIGIN_OF_FUNDS | varchar(100) | 100 | NULL allowed |  |
|  | NAME_OF_PERSON_CONDUCTING_THE_TRANSACTION | varchar(100) | 100 | NULL allowed |  |
|  | RESIDENTIAL_OFFICIAL_ADDRESS_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | NATIONALITY_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | PHONE_NUMBER_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | TYPE_OF_IDENTIFICATION_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | ID_NUMBER_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | ISSUING_AUTHORITY_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | OCCUPATION_3RD_PARTY | varchar(100) | 100 | NULL allowed |  |
|  | TIN_SSNIT | varchar(100) | 100 | NULL allowed |  |
|  | FOCUS_ID | varchar(100) | 100 | NULL allowed |  |


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

## <a name="#usedby"></a>Used By

* [dbo].[spc_ctr_reportdaily_business]


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

