# 📊 Invalid KYC Customers Investigation Report – FAQ

## 📌 Overview

This document explains the SQL query used to identify customers with **invalid, suspicious, incomplete, or poor-quality KYC registrations** within the TIMM CRM system.

The report is designed to support:

- 🛡️ KYC compliance reviews
- 📋 Data quality assessments
- 🔍 Customer registration investigations
- 📊 Regulatory and operational reporting

---

## ❓ What is the purpose of this report?

The report identifies customers whose registration information may be invalid due to:

- Invalid registration status
- Missing names
- Names containing numbers
- Placeholder names (TEST, CLIENT, etc.)
- Repeated characters
- Repeated numbers
- Special characters
- Abnormal name lengths

The objective is to improve customer data quality and ensure compliance with KYC requirements.

---

## ❓ What data source is used?

The report primarily extracts information from:

| Database | Table/View | Purpose |
|-----------|-------------|----------|
| TIMM_CRM | vwc_KYCSubscribersFull | Customer KYC information |
| TIMM_CRM | TbccServicosProvisioningFeatures | Provisioned service features |

---

## ❓ Why is a temporary table used?

A temporary table is created to store all identified problematic records before generating the final report.

```sql
CREATE TABLE #InvalidMISInvestigation
```

Benefits include:

- Improved query readability
- Easier troubleshooting
- Simplified reporting
- Better performance when handling multiple validations

---

## ❓ Which customers are included?

The report only includes customers that meet all of the following conditions:

### Active Service Records

```sql
K.Status != 9
```

### Mobile Service Type

```sql
K.ServiceType = 21
```

### Not Provisioned with Feature 415

```sql
R.ServicoID IS NULL
```

Feature 415 customers are excluded from the report.

---

## ❓ What customer information is captured?

The report stores the following fields:

| Field | Description |
|---------|-------------|
| MSISDN10 | Customer number (10 digits) |
| MSISDN8 | Customer number (8 digits) |
| Client Name | Registered customer name |
| Subscriber Name | SIM subscriber name |
| Type | Customer type |
| GSMValidationClassif | GSM validation category |
| IdentityTypeDesc | Identification type |
| Nacionality | Customer nationality |
| BirthDate | Date of birth |
| FirstUseDate | First service usage date |
| Status | Customer status |

---

## ❓ What validation rules are applied?

The query performs multiple KYC quality checks.

---

## 🔹 1. Invalid Registration

Customers with invalid registration status:

```sql
K.ValidRegistration = 0
```

---

## 🔹 2. Names Containing Numbers

Examples:

```text
John123
Peter45
Mary2025
```

Validation:

```sql
K.[Client Name] LIKE '%[0-9]%'
```

---

## 🔹 3. Missing Client Names

Examples:

```text
NULL
Blank
```

Validation:

```sql
K.[Client Name] IS NULL
```

---

## 🔹 4. Very Short Names

Names with one character or less.

Examples:

```text
A
B
C
```

Validation:

```sql
LEN(LTRIM(RTRIM(ISNULL(K.[Client Name], '')))) <= 1
```

---

## 🔹 5. Very Long Names

Names exceeding 50 characters.

Validation:

```sql
LEN(LTRIM(RTRIM(ISNULL(K.[Client Name], '')))) > 50
```

---

## 🔹 6. Test or Dummy Names

Examples:

```text
TEST USER
TESTE CLIENT
CLIENT ABC
```

Validation includes:

```sql
LIKE '%TEST%'
LIKE '%TESTE%'
LIKE '%DATE%'
LIKE '%CLIENT%'
LIKE '%ABC%'
LIKE '%AZERTY%'
LIKE '%QWERTY%'
```

---

## 🔹 7. Special Characters

Examples:

```text
John_
Mary$
Peter@
Client/
```

Validation:

```sql
LIKE '%[,_./$\@\-()]%'
```

---

## 🔹 8. Repeated Letters

Examples:

```text
AAA JOHN
BBBB TEST
ZZZZ CLIENT
```

The query checks repeated alphabetic patterns from:

```text
AAA through ZZZ
```

Examples:

```sql
LIKE '%AAA%'
LIKE '%BBB%'
LIKE '%CCC%'
...
LIKE '%ZZZ%'
```

---

## 🔹 9. Repeated Numbers

Examples:

```text
000 JOHN
111 TEST
999 CLIENT
```

Checks include:

```sql
LIKE '%000%'
LIKE '%111%'
LIKE '%222%'
...
LIKE '%999%'
```

---

## ❓ Why is Feature 415 excluded?

The query excludes customers provisioned with Feature ID 415:

```sql
AND R.IDFeature = 415
AND R.Status = 1
```

This ensures the report focuses only on customers requiring investigation.

---

## ❓ How is the final report generated?

The final result uses:

```sql
ROW_NUMBER()
```

to generate a sequence number.

```sql
ROW_NUMBER() OVER (
    ORDER BY [Client Name] ASC
)
```

---

## ❓ What fields appear in the final report?

| Column | Description |
|----------|-------------|
| # | Record number |
| MSISDN10 | Customer number |
| MSISDN8 | Alternative customer number |
| Client Name | Registered name |
| Subscriber Name | Subscriber name |
| Type | Customer type |
| GSMValidation Classif | GSM validation category |
| IdentityType Desc | Identity type |
| Nationality | Nationality |
| BirthDate | Date of birth |
| Created_ON | First usage date |
| Status | Customer status |

---

## ❓ How is the report sorted?

Results are sorted alphabetically:

```sql
ORDER BY [Client Name] ASC
```

This makes investigation easier.

---

## ❓ What is the business value of this report?

### Compliance

- Improve KYC compliance
- Support regulatory requirements

### Data Quality

- Remove invalid registrations
- Correct customer records

### Fraud Prevention

- Detect suspicious registrations
- Identify fake customer profiles

### Operational Excellence

- Improve customer database integrity
- Support accurate reporting

---

## 📎 High-Level Process Flow

```text
KYC Customer Base
        │
        ▼
Apply Service Filters
        │
        ▼
Apply KYC Validation Rules
        │
        ▼
Identify Invalid Records
        │
        ▼
Store in Temporary Table
        │
        ▼
Generate Investigation Report
```

---

## ✅ Summary

This report identifies customers with:

- Invalid registration status
- Missing names
- Numeric names
- Placeholder names
- Repeated characters
- Repeated numbers
- Special characters
- Other suspicious KYC patterns

The report serves as a key tool for:

- KYC investigations
- Data cleansing exercises
- Regulatory compliance
- Customer database improvement

---

## 👨‍💻 Author

**James Anointed Morgan Jr.**  
MIS Engineer

**Orange Liberia**
