# 📊 Active Orange Money Customer Base (90 Days) – FAQ

## 📌 Overview

This document explains the SQL query used to calculate the **Active Orange Money Customer Base** over a rolling **90-day period**.

The query identifies unique Orange Money subscribers who performed qualifying financial transactions while excluding reactivation, promotional, and system-generated transactions that do not represent genuine customer activity.

---

## ❓ What is the purpose of this report?

The report calculates the total number of **unique active Orange Money customers** during the previous **90 days**.

It is commonly used to:

- 📊 Measure customer engagement
- 📈 Track Orange Money adoption
- 📉 Monitor customer retention
- 📋 Produce executive KPI reports
- 🎯 Support business performance analysis

---

## ❓ What reporting period does this query use?

The report uses a rolling **90-day window**.

```sql
DECLARE @t1 DATE = '2026-07-07'
DECLARE @t2 DATE = DATEADD(DAY,-90,@t1)
```

Where:

| Variable | Description |
|----------|-------------|
| @t1 | Report Date |
| @t2 | 90 days before the report date |

For this report:

| Variable | Date |
|----------|------------|
| @t1 | 07-Jul-2026 |
| @t2 | 08-Apr-2026 |

The reporting period is therefore:

**08 April 2026 → 07 July 2026**

---

## ❓ What database is used?

All transaction records are retrieved from:

| Database | Table |
|----------|-------|
| DW_OrangeMoney | Transactions |

This table contains all Orange Money financial transactions.

---

# Query Components

The query is divided into three Common Table Expressions (CTEs).

---

## 🔹 1. `reactivation_P2P`

### Purpose

Identifies customer reactivation transactions that should **not** be counted as normal customer activity.

The query searches for customers who:

- Received a promotional Cash-In
- Performed a **10 LRD P2P** transaction shortly afterward

### Filters

```text
Service Type      : P2P
Transaction Tag   : P2P
Status            : TS (Successful)
Currency          : LRD
Amount            : 10 LRD
```

These transactions are excluded from the active customer calculation.

---

## 🔹 2. `reactivation_SP_SO`

### Purpose

Captures promotional and operational transactions that should not contribute to the active customer count.

Included transaction types include:

- Salary Payment
- Special Offer
- Wallet Creation
- Wallet Closure
- Account Creation
- Account Closure
- Operator Withdraw

These transactions are considered system-generated or promotional rather than genuine customer usage.

---

## 🔹 3. `transactions_to_exclude`

### Purpose

Creates a consolidated list of transaction IDs that should be excluded from the final calculation.

The query combines transaction IDs from:

- Reactivation P2P
- Promotional Cash-In
- Salary Payment
- Special Offer
- Wallet Creation/Closure
- Account Creation/Closure

using:

```sql
UNION ALL
```

---

# Final Customer Selection

The final query retrieves subscriber activity from both perspectives.

---

## Sender Activity

Customers who initiated transactions.

```sql
sender_category_code = 'SUBS'
```

---

## Receiver Activity

Customers who received transactions.

```sql
receiver_category_code = 'SUBS'
```

Both datasets are combined using:

```sql
UNION ALL
```

---

## ❓ Why are some transactions excluded?

Before counting active users, the query removes all promotional and reactivation transactions.

```sql
WHERE transfer_id NOT IN (
    SELECT transfer_id
    FROM transactions_to_exclude
)
```

This ensures that only genuine customer activity is considered.

---

## ❓ What qualifies a customer as "Active"?

A customer is considered active if they:

- Performed at least one successful transaction
- Are classified as a subscriber (`SUBS`)
- Transacted within the last **90 days**
- Did not participate exclusively in promotional or reactivation transactions

---

## ❓ What transaction status is accepted?

Only successful transactions are included.

```sql
transfer_status = 'TS'
```

Meaning:

| Status | Meaning |
|---------|----------|
| TS | Successful Transaction |

---

## ❓ Which currency is considered?

The promotional filtering logic considers transactions in:

```text
LRD
```

---

## ❓ Why is `COUNT(DISTINCT)` used?

```sql
COUNT(DISTINCT(msisdn))
```

This guarantees that every subscriber is counted only once regardless of the number of transactions performed.

Example:

| MSISDN | Transactions |
|---------|--------------|
| 0777000001 | 54 |

Result:

```text
Active Customer = 1
```

---

## ❓ What is the final output?

| Column | Description |
|---------|-------------|
| active_users | Total unique active Orange Money subscribers over the last 90 days |

---

## ❓ Why are wallet creation and closure transactions excluded?

These activities do not represent actual customer usage.

Excluded transaction types include:

- Wallet Creation
- Wallet Closure
- Account Creation
- Account Closure
- Operator Withdraw

Removing these events provides a more accurate measure of customer activity.

---

## ❓ What is the business value of this report?

The report supports:

- 📊 Monthly and quarterly KPI reporting
- 📈 Customer engagement analysis
- 💰 Orange Money growth monitoring
- 📉 Retention analysis
- 🎯 Business strategy and planning
- 📋 Executive dashboards

---

# High-Level Process Flow

```text
Orange Money Transactions
            │
            ▼
Retrieve Last 90 Days
            │
            ▼
Identify Reactivation Transactions
            │
            ▼
Identify Promotional Transactions
            │
            ▼
Exclude Non-Organic Transactions
            │
            ▼
Retrieve Genuine Subscriber Activity
            │
            ▼
Count Unique Active Customers
```

---

## 📎 Full SQL Script

```sql
-- DECLARE @t1 DATE = '2026-07-07' 
DECLARE @t2 DATE = dateadd(day,-90, @t1);

  WITH reactivation_P2P AS (
    SELECT DISTINCT 
           A.*,
           B.sender_msisdn sd_msisdn,
           B.transfer_id txn_id,
           B.transaction_amount txn_amt
    FROM (
        SELECT 
               refdate,
               transfer_datetime,
               sender_msisdn,
               sender_user_id,
               sender_user_name,
               receiver_msisdn,
               receiver_user_id,
               receiver_user_name,
               service_type,
               transaction_tag,
               transfer_status,
               transfer_id,
               currencytype,
               transaction_amount
        FROM [DW_OrangeMoney].[dbo].[Transactions] WITH (NOLOCK) 
        WHERE refdate >= @t2
          AND refdate <= @t1  
          AND service_type = 'P2P'
          AND transaction_tag = 'P2P'
          AND transfer_status = 'TS'
          AND currencytype = 'LRD'
          AND transaction_amount = 10
    ) A
    INNER JOIN (
        SELECT 
               refdate,
               transfer_datetime,
               sender_msisdn,
               sender_user_id,
               sender_user_name,
               receiver_msisdn,
               receiver_user_id,
               receiver_user_name,
               service_type,
               transaction_tag,
               transfer_status,
               transfer_id,
               currencytype,
               transaction_amount
        FROM [DW_OrangeMoney].[dbo].[Transactions] WITH (NOLOCK) 
        WHERE refdate >= @t2
          AND refdate <= @t1
          AND transfer_status = 'TS'
          AND sender_msisdn IN ('0779760014','0779760013')
          AND service_type = 'CASHIN'
          AND transaction_tag = 'CASHIN'
          AND currencytype = 'LRD'
    ) B ON A.sender_msisdn = B.receiver_msisdn
),
reactivation_SP_SO AS (
    SELECT 
           refdate,
           transfer_datetime,
           sender_msisdn,
           sender_user_id,
           sender_user_name,
           receiver_msisdn,
           receiver_user_id,
           receiver_user_name,
           service_type,
           transaction_tag,
           transfer_status,
           transfer_id,
           currencytype,
           transaction_amount
    FROM [DW_OrangeMoney].[dbo].[Transactions] WITH (NOLOCK) 
    WHERE refdate >= @t2
      AND refdate <= @t1
      AND (
            (
                (sender_msisdn = '0779740903' AND service_type = 'ENT2REG' AND transaction_tag = 'SALARY PAYMENT')
             OR (sender_msisdn = '0779802622' AND service_type = 'CASHIN' AND transaction_tag = 'SPECIAL OFFER')
            )
            AND currencytype = 'LRD'
            AND transaction_amount <= 30
          )
      OR transaction_tag IN ('WALLET CLOSURE', 'WALLET CREATION', 'ACCOUNT CREATION', 'ACCOUNT CLOSURE','OPERATOR WITHDRAW')
      AND transfer_status = 'TS'
),
transactions_to_exclude AS (
    SELECT DISTINCT transfer_id
    FROM (
        SELECT transfer_id FROM reactivation_P2P
        UNION ALL
        SELECT txn_id FROM reactivation_P2P
        UNION ALL
        SELECT transfer_id FROM reactivation_SP_SO
    ) A
)
SELECT COUNT(DISTINCT(msisdn)) AS active_users
FROM (
    SELECT DISTINCT 
           A.msisdn
    FROM (
        SELECT 
               refdate,
               sender_msisdn AS msisdn,
               sender_category_code AS category_code,
               transaction_tag,
               transfer_id,
               currencytype,
               transaction_amount
        FROM [DW_OrangeMoney].[dbo].[transactions] WITH (NOLOCK) 
        WHERE transfer_status = 'TS' 
          AND refdate >= @t2
          AND refdate <= @t1
          AND sender_category_code = 'SUBS'
        UNION ALL
        SELECT 
               refdate,
               receiver_msisdn AS msisdn,
               receiver_category_code AS category_code,
               transaction_tag,
               transfer_id,
               currencytype,
               transaction_amount
        FROM [DW_OrangeMoney].[dbo].[transactions]
        WHERE transfer_status = 'TS' 
          AND refdate >= @t2
          AND refdate <= @t1
          AND receiver_category_code = 'SUBS'
    ) A
    WHERE transfer_id NOT IN (SELECT transfer_id FROM transactions_to_exclude WITH (NOLOCK) )
) B;
```

---

## ❓ Difference Between the 30-Day and 90-Day Reports

| Feature | 30-Day Report | 90-Day Report |
|----------|---------------|---------------|
| Reporting Window | Last 30 Days | Last 90 Days |
| Logic | Same | Same |
| Exclusions | Same | Same |
| Output | Active Users | Active Users |
| KPI Purpose | Monthly Activity | Quarterly Activity |

---

## ✅ Summary

This query:

- Retrieves Orange Money transactions over the previous **90 days**
- Excludes promotional and reactivation transactions
- Removes wallet creation and closure events
- Counts unique subscribers who performed genuine financial activity

The resulting figure represents the official **90-Day Active Orange Money Customer Base**.

---

## 👨‍💻 Author

**James Anointed Morgan Jr.**  
MIS Engineer  
Orange Liberia
