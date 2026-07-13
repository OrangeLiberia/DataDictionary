# 📊 Active Orange Money Customer Base (30 Days) - FAQ

## 📌 Overview

This document explains the SQL query used to calculate the **Active Orange Money Customer Base** over a rolling **30-day period**.

The query identifies unique Orange Money subscribers who performed qualifying financial transactions while excluding transactions related to customer reactivation, promotional campaigns, wallet creation/closure, and other non-organic activities.

---

## ❓ What is the purpose of this report?

The report calculates the number of **unique active Orange Money customers** within the last **30 days**.

It is used to:

- 📊 Measure the active Orange Money customer base
- 📈 Monitor customer engagement
- 🎯 Track business performance
- 📋 Produce management and regulatory reports

---

## ❓ What reporting period does this query use?

The reporting window is dynamic.

```sql
DECLARE @t1 DATE = '2026-07-07'
DECLARE @t2 DATE = DATEADD(DAY,-30,@t1)
```

Where:

- **@t1** = Report Date
- **@t2** = 30 days before the report date

In this example:

| Variable | Date |
|----------|------------|
| @t1 | 07-Jul-2026 |
| @t2 | 07-Jun-2026 |

The report therefore covers:

**07 June 2026 → 07 July 2026**

---

## ❓ What transaction database is used?

The query retrieves transactions from:

| Database | Table |
|----------|-------|
| DW_OrangeMoney | Transactions |

This table stores all Orange Money transaction records.

---

# Query Components

The query is divided into three Common Table Expressions (CTEs).

---

## 🔹 1. `reactivation_P2P`

### Purpose

Identifies **reactivation transactions** that should **NOT** count as customer activity.

The query searches for customers who:

- Received a promotional Cash-In
- Immediately performed a P2P transfer of **10 LRD**

### Filters

```text
Service Type : P2P
Transaction Tag : P2P
Status : Successful (TS)
Currency : LRD
Amount : 10 LRD
```

It then matches those transactions with promotional Cash-In records.

---

## 🔹 2. `reactivation_SP_SO`

### Purpose

Captures promotional and system-generated transactions that should also be excluded.

Included transaction types:

- Salary Payment
- Special Offer
- Wallet Creation
- Wallet Closure
- Account Creation
- Account Closure
- Operator Withdraw

These activities are not considered genuine customer usage.

---

## 🔹 3. `transactions_to_exclude`

### Purpose

Combines all excluded transaction IDs into one list.

```sql
UNION ALL
```

is used to merge:

- Reactivation P2P transactions
- Promotional transactions
- Special Offer transactions

This list is later used to remove non-organic activity.

---

# Final Customer Selection

The final query extracts subscribers from two perspectives.

---

## Sender Activity

```sql
sender_category_code = 'SUBS'
```

Customers who initiated transactions.

---

## Receiver Activity

```sql
receiver_category_code = 'SUBS'
```

Customers who received transactions.

Both datasets are combined using:

```sql
UNION ALL
```

---

## ❓ Why are excluded transactions removed?

Before counting active users, the query removes all transactions found in:

```sql
transactions_to_exclude
```

using

```sql
WHERE transfer_id NOT IN (...)
```

This ensures that promotional and artificial transactions do not inflate the active customer base.

---

## ❓ What qualifies a customer as "Active"?

A customer is considered active if they:

- Performed at least one successful transaction
- Are classified as a subscriber (`SUBS`)
- Transacted within the last 30 days
- Did not participate only in excluded promotional/reactivation activities

---

## ❓ What transaction status is accepted?

Only successful transactions are counted.

```sql
transfer_status = 'TS'
```

Meaning:

| Status | Meaning |
|---------|----------|
| TS | Successful Transaction |

---

## ❓ Which currency is included?

Only transactions in:

```text
LRD
```

are considered for the promotional filtering logic.

---

## ❓ Why is `COUNT(DISTINCT)` used?

```sql
COUNT(DISTINCT(msisdn))
```

This ensures each customer is counted only once, regardless of how many transactions they performed.

Example:

| MSISDN | Transactions |
|---------|--------------|
| 0777XXXXXX | 18 |

Result:

```text
Active Customers = 1
```

---

## ❓ What is the final output?

| Column | Description |
|---------|-------------|
| active_users | Total unique active Orange Money subscribers |

---

## ❓ Why are wallet creation and closure excluded?

The following transaction types do not represent genuine customer usage:

- Wallet Creation
- Wallet Closure
- Account Creation
- Account Closure
- Operator Withdraw

Including them would artificially increase the active customer count.

---

## ❓ What is the business value of this report?

This report helps the business:

- 📈 Measure customer engagement
- 📊 Track monthly active users
- 💰 Evaluate Orange Money adoption
- 📉 Monitor customer retention
- 🎯 Support KPI reporting
- 📋 Produce executive dashboards

---

# High-Level Process Flow

```text
Orange Money Transactions
            │
            ▼
Retrieve Last 30 Days
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
DECLARE @t2 DATE = dateadd(day,-30, @t1);

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

## ✅ Summary

This query:

- Retrieves Orange Money transactions from the last 30 days
- Removes promotional and reactivation transactions
- Removes wallet creation and closure events
- Counts unique subscribers who performed genuine financial activity

The result represents the official **30-Day Active Orange Money Customer Base**.

---

## 👨‍💻 Author

**James Anointed Morgan Jr.**  
MIS Engineer  
Orange Liberia
