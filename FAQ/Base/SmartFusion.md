# 📊 Smart Fusion Inactive Base Report – FAQ

## 📌 Overview
This document provides answers to frequently asked questions about the **Smart Fusion Inactive Base Report**, including how the data is generated, filtered, and interpreted.

---

## ❓ What is the Smart Fusion Inactive Base Report?
The Smart Fusion Inactive Base Report identifies customers who previously purchased Smart Fusion bundles but are currently considered inactive based on bundle expiration.

---

## ❓ What defines an “inactive” customer in this report?
A customer is classified as inactive if:
- Their **bundle expiration date is older than 2 months** from today.
- They have made at least one bundle purchase within the **last 6 months**.

---

## ❓ What data fields are included in the report?

| Field Name        | Description |
|------------------|-------------|
| MobileNumber     | Customer’s phone number (MSISDN) |
| BundleID         | Unique identifier for the bundle |
| BundleName       | Name of the bundle |
| PurchaseDate     | Date the bundle was purchased |
| PurchaseAmount   | Cost of the bundle |
| ExpirationDate   | Date the bundle expired |

---

## ❓ What data sources are used?
The report pulls data from the following tables:

- `tbc_V9CampaignsBundleDR` (Transaction data)
- `tbc_BundleID` (Bundle reference data)

These tables are joined using the `BundleID` field.

---

## ❓ How are bundles selected for this report?
Only specific Smart Fusion bundles are included using predefined **Bundle IDs**:


4000141, 4000142, 4000149, 4000150,
4000348, 4000349, 4000207, 4000205,
4000208, 4000209, 4000206,
10065, 10066, 10067, 10068,
10078, 10079, 10080, 10081, 10082,
10399, 10404


---

## ❓ What filters are applied in this report?

### 🔹 Expiration Filter
Only bundles that expired **at least 2 months ago** are included:

```sql
T.Expiration_Date <= DATEADD(MONTH, -2, GETDATE())
🔹 Purchase Filter

Only bundles purchased within the last 6 months are included:

T.Event_Date >= DATEADD(MONTH, -6, GETDATE())
❓ Why is DISTINCT used in the query?

DISTINCT ensures that duplicate records are removed, so each row in the report is unique.

❓ Why is an INNER JOIN used?

An INNER JOIN ensures:

Only records with matching BundleID in both tables are included
Each transaction is properly linked to its bundle name
❓ How is the data sorted?
ORDER BY T.Expiration_Date DESC

This ensures the most recently expired bundles appear first.

❓ What is the business use of this report?
📣 Targeted reactivation campaigns
📉 Identifying churned Smart Fusion users
📊 Customer behavior analysis
🎯 Marketing segmentation
❓ Can the query be modified?

Yes, the query can be adjusted to:

Change inactivity duration (e.g., 1 month instead of 2)
Expand or reduce bundle IDs
Extend or shorten the purchase window
Add more customer attributes if needed
📎 SQL Query Reference
SELECT DISTINCT
    T.MSISDN           AS MobileNumber,
    T.BundleID         AS BundleID,
    A.Name             AS BundleName,
    T.Event_Date       AS PurchaseDate,
    T.BundleCost       AS PurchaseAmount,
    T.Expiration_Date  AS ExpirationDate
FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR] T
INNER JOIN [TIMM_Report].[dbo].[tbc_BundleID] A 
    ON T.BundleID = A.BundleID
WHERE T.BundleID IN (
    4000141, 4000142, 4000149, 4000150,
    4000348, 4000349, 4000207, 4000205,
    4000208, 4000209, 4000206,
    10065, 10066, 10067, 10068,
    10078, 10079, 10080, 10081, 10082,
    10399, 10404
)
AND T.Expiration_Date <= DATEADD(MONTH, -2, GETDATE())
AND T.Event_Date >= DATEADD(MONTH, -6, GETDATE())
ORDER BY T.Expiration_Date DESC;
✅ Summary

The Smart Fusion Inactive Base Report helps identify users who:

Recently engaged with Smart Fusion bundles
But have not renewed after expiration

This enables data-driven decision-making for customer retention and marketing strategies.

👨‍💻 Author
Randy Xarri George.
MIS Engineer
