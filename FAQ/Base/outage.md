# 📊 Subscriber Outage Analysis – FAQ

---

## ❓ What does this analysis do?

This analysis identifies **subscribers affected by a network outage** and determines **which bundles they were using during the outage period**.

---

## ❓ How are affected subscribers identified?

```sql
SELECT [MSISDN]
INTO #Temp
FROM [TIMM_Report].[dbo].[SubsLocationTracking]
WHERE siteid IN 
('9233', ...) -- List of site IDs impacted by the outage
AND RefDate = '2026-03-18' -- Date of interest (outage day)
GROUP BY MSISDN;
```

### 💡 Answer

* Extracts **unique subscriber phone numbers (MSISDN)**.
* Filters users connected to **specific impacted sites**.
* Limits results to the **outage date**.
* Stores results in a **temporary table (`#Temp`)** for reuse.

---

## ❓ How are affected bundles identified?

```sql
SELECT Name, T.msisdn, T.BUNDLEID
FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR] T
INNER JOIN [TIMM_Report].[dbo].[tbc_BundleID] A
ON T.BUNDLEID = A.BundleID
WHERE Action = 8 
  AND Enabled = 1
  AND Event_Date BETWEEN '2025-01-01 17:00:00' AND '2026-03-18 10:51:32'
  AND Expiration_Date BETWEEN '2026-03-18 10:51:32' AND '2026-03-18 14:10:16'
  AND MSISDN IN (SELECT RIGHT(MSISDN, 9) FROM #Temp)
  AND T.BundleID NOT IN (205)
GROUP BY A.Name, T.msisdn, T.BUNDLEID
ORDER BY 2;
```

### 💡 Answer

* Joins subscriber bundle usage with **bundle metadata**.
* Filters only:

  * **Valid transactions** (`Action = 8`, `Enabled = 1`)
  * Activity before and during the outage
  * Bundles that **expired during the outage window**
* Matches only subscribers identified in **Step 1**.
* Excludes specific bundles (e.g., `205`).

---

## ❓ Why is a temporary table used?

The temporary table `#Temp`:

* Stores affected subscribers once.
* Improves readability and reuse in subsequent queries.
* Avoids recalculating the same dataset multiple times.

---

## ❓ Why is `RIGHT(MSISDN, 9)` used?

* Ensures **consistent phone number format**.
* Matches MSISDN values between tables when formats differ (e.g., with/without country code).

---

## ❓ What is the outage time window used?

* **Outage Start:** `2026-03-18 10:51:32`
* **Outage End:** `2026-03-18 14:10:16`

This window is used to:

* Identify bundles **active before the outage**
* Detect bundles that **expired during the outage**

---

## ❓ What is the final output?

The result provides:

* **Subscriber number (MSISDN)**
* **Bundle ID**
* **Bundle name**

This helps in:

* Measuring customer impact
* Supporting compensation decisions
* Reporting outage effects

---
