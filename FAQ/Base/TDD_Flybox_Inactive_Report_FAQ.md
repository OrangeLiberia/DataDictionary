# 📊 Inactive TDD Flybox Customers Report (Jan–Feb 2026) – FAQ

## 📌 Overview

This document explains the logic and structure used to generate the report for **Inactive TDD Flybox customers** during **January–February 2026**.

---

##  What is the purpose of this report?

The report identifies **TDD Flybox customers who were previously active but showed no activity during Jan–Feb 2026**.

It supports:

- 📉 Customer churn analysis  
- 📣 Reactivation campaigns  
- 📊 Business decision-making  

---

##  What defines an “inactive” customer in this script?

A customer is considered inactive if:

- They were part of the **historical TDD Flybox base (before Jan 2026)**  
- They had **NO activity during Jan–Feb 2026**  

---

##  How are TDD Flybox bundles identified?

Bundles are filtered using:

```sql
WHERE [GlobalName] LIKE '%Flybox%' 
   OR [Name] LIKE '%TDD%'

👉 This ensures only Flybox / TDD-related bundles are included.

 What is the logic behind each CTE (Common Table Expression)?
🔹 1. TDD_Flybox_Bundles
SELECT [BundleID], [Name], [GlobalName]
FROM [TIMM_Report].[dbo].[tbc_BundleID]
WHERE [GlobalName] LIKE '%Flybox%' 
   OR [Name] LIKE '%TDD%'

👉 Identifies all relevant Flybox/TDD bundles.

🔹 2. Active_In_Period
SELECT DISTINCT [MSISDN]
FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR]
WHERE [BundleID] IN (SELECT [BundleID] FROM TDD_Flybox_Bundles)
  AND (
      [Event_Date] BETWEEN '2026-01-01' AND '2026-02-28' 
      OR [Expiration_Date] >= '2026-01-01'
  )

👉 Captures customers who were active during Jan–Feb 2026.

Activity is defined as:

A purchase within the period
OR a bundle still valid into the period
🔹 3. Historical_Base
SELECT DISTINCT [MSISDN]
FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR]
WHERE [BundleID] IN (SELECT [BundleID] FROM TDD_Flybox_Bundles)
  AND [Event_Date] < '2026-01-01'

👉 Identifies customers who used Flybox before Jan 2026 and forms the base population.

 How are inactive customers identified?
LEFT JOIN Active_In_Period A ON H.MSISDN = A.MSISDN
WHERE A.MSISDN IS NULL

👉 This means:

Customers in the historical base
BUT NOT found in active users during Jan–Feb

✔️ These are classified as inactive

 Why is the latest activity (MAX Event_Date) used?
DR.Event_Date = (
    SELECT MAX(Event_Date) 
    FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR] 
    WHERE MSISDN = H.MSISDN
)
Ensures only the most recent bundle record per customer is selected
Prevents duplicate or outdated records
 What fields are returned in the final output?
Field Name	Description
MSISDN	Customer phone number
Status	Always marked as “Inactive”
Inactivity_Duration	Fixed at 59 days (Jan + Feb)
Last_Known_Bundle	Last bundle used
GlobalName	Bundle category
 Why is inactivity duration set to 59 days?
'59 Days'
January = 31 days
February = 28 days

👉 Total = 59 days


❓ What is the business value of this report?
📣 Target users for Flybox reactivation campaigns
📊 Identify churn trends in fixed broadband usage
🎯 Improve retention strategies
💡 Optimize bundle offerings
❓ Can this script be improved?

Yes, possible enhancements include:

Include March activity check explicitly
Add revenue or ARPU fields
Segment by location or usage pattern
Parameterize date ranges
📎 Full SQL Script
WITH TDD_Flybox_Bundles AS (
    SELECT [BundleID], [Name], [GlobalName]
    FROM [TIMM_Report].[dbo].[tbc_BundleID]
    WHERE [GlobalName] LIKE '%Flybox%' OR [Name] LIKE '%TDD%'
),
Active_In_Period AS (
    SELECT DISTINCT [MSISDN]
    FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR]
    WHERE [BundleID] IN (SELECT [BundleID] FROM TDD_Flybox_Bundles)
      AND (
          [Event_Date] BETWEEN '2026-01-01' AND '2026-02-28' 
          OR [Expiration_Date] >= '2026-01-01'
      )
),
Historical_Base AS (
    SELECT DISTINCT [MSISDN]
    FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR]
    WHERE [BundleID] IN (SELECT [BundleID] FROM TDD_Flybox_Bundles)
      AND [Event_Date] < '2026-01-01'
)
SELECT 
    [ID],
    H.[MSISDN],
    'Inactive' AS [Jan_Feb&March_2026_Status],
    '59 Days' AS [Inactivity_Duration],
    B.[Name] AS [Last_Known_Bundle],
    B.[GlobalName]
FROM Historical_Base H
JOIN [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR] DR ON H.MSISDN = DR.MSISDN
JOIN TDD_Flybox_Bundles B ON DR.BundleID = B.BundleID
LEFT JOIN Active_In_Period A ON H.MSISDN = A.MSISDN
WHERE A.MSISDN IS NULL
  AND DR.Event_Date = (
      SELECT MAX(Event_Date) 
      FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR] 
      WHERE MSISDN = H.MSISDN
  )
ORDER BY H.MSISDN;

✅ Summary
This script:
Builds a historical base of Flybox users
Checks activity during Jan–Feb 2026
Flags users with no activity as inactive
Returns their last known bundle

Result: A clean dataset of churned TDD Flybox customers

👨‍💻 Author
James Anointed Morgan Jr.
MIS Engineer
