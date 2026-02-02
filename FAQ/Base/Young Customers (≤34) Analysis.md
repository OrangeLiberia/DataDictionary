# Young Customers (≤34) Analysis

**Purpose**
This document explains the SQL script `young_customers_analysis.sql` used to build a temporary dataset of customers aged **less than or equal to 34** and to compute a set of standard metrics (ARPU, usage, bundles, activity status). It also provides a short FAQ and troubleshooting guide so any team member can run, modify, or debug the script and understand defensive conversions added to avoid `varchar -> numeric` errors (SQL Server `Msg 8114`).

---

## Summary of the Report

* Build a temporary base of subscribers whose age is **≤ 34**.
* Produce analyses: counts, device breakdown, location distribution, monthly ARPU/AUPU/AAPU, favorite bundles, consumption patterns, active vs inactive segmentation, and a monthly summary dashboard.
* Apply defensive parsing and conversions to avoid runtime errors when numeric columns are stored as text (e.g., `ARPU`, `BundleCost`, `MB`, `DURATION`).

---

## Prerequisites

* SQL Server 2012 or newer (required for `TRY_CONVERT`).
* Access to the following source tables/views in the `TIMM_Report` database:

  * `SubscribersDailyExport`
  * `tbc_V9CampaignsBundleDR`
  * `tbc_BundleID`
  * `xDRData`
  * `xDRVoice`
  * `County_PowerBi_vf`
* Appropriate read permissions to run SELECT queries against these objects.

---

## How to run (recommended safe steps)

1. Open the `young_customers_analysis.sql` script in SQL Server Management Studio (SSMS) or your SQL editor.
2. Optionally change the date range by editing `@StartDate` and `@EndDate` at the top of the script.
3. Run the script in a development or staging environment first.
4. Inspect outputs and identify any rows where conversions produced `NULL` (diagnostic queries are provided below).

**Note:** The script drops temporary tables at the end; if you want to inspect intermediate results, comment out the cleanup `DROP TABLE` statements.

---

## Quick query — list customers (MSISDN + DOB) only

If you want just the list of customers aged ≤34 (no counts), run the following, which assumes the `#young_customers` temp table exists in the session:

```sql
SELECT DISTINCT
  MSISDN,
  CONVERT(CHAR(10), DateOfBirth, 120) AS DateOfBirth
FROM #young_customers
WHERE Age IS NOT NULL
  AND Age <= 34
ORDER BY DateOfBirth ASC, MSISDN;
```

If `#young_customers` is not present, run this direct-from-source version:

```sql
DECLARE @CurrentDate DATE = '2025-11-28';

SELECT DISTINCT
  MSISDN,
  CONVERT(CHAR(10), TRY_CONVERT(DATE, DOB), 120) AS DateOfBirth
FROM [TIMM_Report].[dbo].[SubscribersDailyExport]
WHERE TRY_CONVERT(DATE, DOB) IS NOT NULL
  AND DATEDIFF(YEAR, TRY_CONVERT(DATE, DOB), @CurrentDate) <= 34
  AND MSISDN IS NOT NULL
ORDER BY DateOfBirth ASC, MSISDN;
```

---

## Diagnostics — find problematic (non-numeric) rows

If you suspect conversion problems (e.g., `BundleCost`, `ARPU`, `MB`, `DURATION`) use these diagnostic queries to inspect problematic source values:

**ARPU / VoiceARPU / DataARPU problems**

```sql
SELECT TOP 100 MSISDN, ARPU, VoiceARPU, DataARPU
FROM [TIMM_Report].[dbo].[SubscribersDailyExport]
WHERE (ARPU IS NOT NULL AND TRY_CONVERT(DECIMAL(18,2), REPLACE(REPLACE(LTRIM(RTRIM(ARPU)), ',', ''), CHAR(160), '')) IS NULL)
   OR (VoiceARPU IS NOT NULL AND TRY_CONVERT(DECIMAL(18,2), REPLACE(REPLACE(LTRIM(RTRIM(VoiceARPU)), ',', ''), CHAR(160), '')) IS NULL)
   OR (DataARPU IS NOT NULL AND TRY_CONVERT(DECIMAL(18,2), REPLACE(REPLACE(LTRIM(RTRIM(DataARPU)), ',', ''), CHAR(160), '')) IS NULL);
```

**BundleCost problems**

```sql
SELECT TOP 100 BundleID, BundleCost
FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR]
WHERE BundleCost IS NOT NULL
  AND TRY_CONVERT(DECIMAL(18,2), REPLACE(REPLACE(LTRIM(RTRIM(BundleCost)), ',', ''), CHAR(160), '')) IS NULL;
```

Run those diagnostics to identify rows that need cleaning at the source or special handling.

---

## FAQ

**Q: Why does the script use `TRY_CONVERT` instead of `CONVERT`?**
A: `TRY_CONVERT` returns `NULL` for values that cannot be converted and thus avoids runtime conversion errors (Msg 8114). `CONVERT` would raise an error if it encounters a non-numeric string.

**Q: Why are commas and `CHAR(160)` being removed?**
A: Commas (thousand separators) and non-breaking spaces (common when data is exported from Excel) are non-numeric characters that cause conversion failures. Removing them improves successful conversions.

**Q: The aggregates show lower totals after `TRY_CONVERT`. Why?**
A: Non-numeric values become `NULL` during conversion and we used `COALESCE(..., 0)` in SUMs. If many values are non-numeric, the true monetary totals may be underestimated. Prefer cleaning at source if possible.

**Q: I need zero instead of NULL for invalid numeric values. How do I change that?**
A: The script already uses `COALESCE(..., 0)` where appropriate for sums. If you want every numeric column to become `0` (not just aggregates), wrap `TRY_CONVERT(..., ...)` in `COALESCE(..., 0)` where you select or insert.

**Q: My SQL Server is older than 2012 and doesn’t have `TRY_CONVERT`. What do I do?**
A: Use `ISNUMERIC()` with caution or create a pattern-based check (e.g., `LIKE` to allow only `[0-9]` and `.`) before converting. Contact the team for a tailored fallback.

---

## Appendix: Useful snippets

* To inspect converted rows (which became `NULL`) for `BundleCost`:

```sql
SELECT TOP 100 BundleID, BundleCost
FROM [TIMM_Report].[dbo].[tbc_V9CampaignsBundleDR]
WHERE BundleCost IS NOT NULL
  AND TRY_CONVERT(DECIMAL(18,2), REPLACE(REPLACE(LTRIM(RTRIM(BundleCost)), ',', ''), CHAR(160), '')) IS NULL;
```


