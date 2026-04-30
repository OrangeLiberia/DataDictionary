# 📊 Long-Term Active Customers Report (5+ Years) – FAQ

##  Overview
This document explains the SQL logic used to identify **customers who joined the network over 5 years ago and are still active in the last 3 months of 2026**.

---

## What is the purpose of this report?

The report identifies **loyal customers** who:

- Joined the network **before April 1, 2021**  
- Remained **active from January 2026 onwards**  

👉 This helps the business recognize and analyze **long-term retained users**.

---

##  What defines a “5+ year customer”?

A customer is considered a 5+ year user if:

```sql
PrimeiroUsoEM <= '2021-04-01' 
AND DataCriacao <= '2021-04-01'
PrimeiroUsoEM → First usage date
DataCriacao → Account creation date

👉 Ensures the customer has been on the network for at least 5 years.

 What defines an “active customer” in this report?

A customer is considered active if:

[BILastActivity] >= '2026-01-01'

👉 This means:

The customer has activity in January, February, or March 2026
 What is the logic behind the query?
🔹 Step 1: Identify 5+ Year Customers
SELECT DISTINCT S.MSISDN
INTO #msisdn1
FROM [timm.CRM].TIMM_CRM.dbo.TIMM_Servicos S 
WHERE PrimeiroUsoEM <= '2021-04-01' 
  AND DataCriacao <= '2021-04-01'

👉 Creates a temporary table #msisdn1 containing long-term customers.

🔹 Step 2: Identify Recently Active Customers
SELECT DISTINCT MSISDN8 AS MSISDN
INTO #msisdn2
FROM [Repository202603].[crm].[FullCRMSubsBase]
WHERE [BILastActivity] >= '2026-01-01'

👉 Creates a temporary table #msisdn2 with customers active in the last 3 months.

🔹 Step 3: Get Final Result (Intersection)
SELECT *
FROM #msisdn1 
WHERE MSISDN IN (SELECT MSISDN FROM #msisdn2)

👉 Returns customers who:

Are 5+ years old on the network
AND still active in 2026 (Q1)
 What is the output of this report?
Field Name	Description
MSISDN	Customer phone number

👉 The result is a list of loyal, long-term active customers.

 Why is this report important?
🎯 Identify high-value loyal customers
📊 Measure customer retention over time
🎁 Support loyalty reward programs
📣 Target users for exclusive offers

Can this query be improved?

Yes, possible enhancements include:

Add ARPU or revenue data
Include customer segmentation (region, plan)
Track usage trends over time
Convert temp tables into CTEs for cleaner structure

📎 Full SQL Script
-- Customers created more than 5 years ago
SELECT DISTINCT S.MSISDN
INTO #msisdn1
FROM [timm.CRM].TIMM_CRM.dbo.TIMM_Servicos S 
WHERE PrimeiroUsoEM <= '2021-04-01' 
  AND DataCriacao <= '2021-04-01';

-- Customers active in the last 3 months (Jan–Mar 2026)
SELECT DISTINCT MSISDN8 AS MSISDN
INTO #msisdn2
FROM [Repository202603].[crm].[FullCRMSubsBase]
WHERE [BILastActivity] >= '2026-01-01';

-- Final result: 5+ year customers still active
SELECT *
FROM #msisdn1 
WHERE MSISDN IN (SELECT MSISDN FROM #msisdn2);

✅ Summary
This script:
Identifies customers who joined 5+ years ago
Filters those who are still active in Q1 2026
Returns a list of loyal, retained users

👉 Result: A valuable dataset for customer retention and loyalty analysis

👨‍💻 Author
James Anointed Morgan Jr.
MIS Engineer
