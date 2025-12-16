# Paygo International Calls Report

## Overview
This report extracts customer data for Paygo international calls made to specified destination countries over the last 3 months.

## Request Details
- **Requested By:** Lisa Verin
- **Date:** December 16, 2025
- **Data Period:** Last 3 months (September 16, 2025 – December 16, 2025)

## Target Countries

| Country | Country Code |
|---------|--------------|
| Bangladesh | +880 |
| China | +86 |
| France | +33 |
| Ghana | +233 |
| Guinea | +224 |
| India | +91 |
| Ivory Coast (Côte d'Ivoire) | +225 |
| Lebanon | +961 |
| Mali | +223 |
| Senegal | +221 |
| Sierra Leone | +232 |
| USA | +1 |
| Nigeria | +234 |
| UK (United Kingdom) | +44 |
| Saudi Arabia | +966 |
| Pakistan | +92 |
| Canada | +1 |
| Portugal | +351 |
| Germany | +49 |
| Italy | +39 |
| Burkina Faso | +226 |

## Data Source
- **Database:** TIMM_Report
- **Table:** xDRVoice

## Output Columns

| Column | Description |
|--------|-------------|
| Customer Billing Number | The billing number associated with the customer |
| Calling Number | The originating phone number |
| Called International Number | The international destination number called |
| Destination Country | Country name derived from the called number prefix |
| Country Code | International dialing code of the destination |
| Customer Type | B2B or B2C classification |
| Total Calls | Count of calls made to the destination |
| Total Duration (Seconds) | Sum of call durations in seconds |
| Total Charged Amount | Total amount charged for the calls |
| First Call Date | Earliest call date in the period |
| Last Call Date | Most recent call date in the period |

## SQL Query

```sql
-- Customers with Paygo International Calls to Specified Countries (Last 3 Months)
-- Ready for stakeholder delivery

SELECT DISTINCT
    BILLING_NBR AS [Customer Billing Number],
    CALLING_NBR AS [Calling Number],
    CALLED_NBR AS [Called International Number],
    CASE 
        WHEN CALLED_NBR LIKE '880%' THEN 'Bangladesh'
        WHEN CALLED_NBR LIKE '86%' THEN 'China'
        WHEN CALLED_NBR LIKE '33%' THEN 'France'
        WHEN CALLED_NBR LIKE '233%' THEN 'Ghana'
        WHEN CALLED_NBR LIKE '224%' THEN 'Guinea'
        WHEN CALLED_NBR LIKE '91%' THEN 'India'
        WHEN CALLED_NBR LIKE '225%' THEN 'Ivory Coast'
        WHEN CALLED_NBR LIKE '961%' THEN 'Lebanon'
        WHEN CALLED_NBR LIKE '223%' THEN 'Mali'
        WHEN CALLED_NBR LIKE '221%' THEN 'Senegal'
        WHEN CALLED_NBR LIKE '232%' THEN 'Sierra Leone'
        WHEN CALLED_NBR LIKE '1%' THEN 'USA/Canada'
        WHEN CALLED_NBR LIKE '234%' THEN 'Nigeria'
        WHEN CALLED_NBR LIKE '44%' THEN 'UK'
        WHEN CALLED_NBR LIKE '966%' THEN 'Saudi Arabia'
        WHEN CALLED_NBR LIKE '92%' THEN 'Pakistan'
        WHEN CALLED_NBR LIKE '351%' THEN 'Portugal'
        WHEN CALLED_NBR LIKE '49%' THEN 'Germany'
        WHEN CALLED_NBR LIKE '39%' THEN 'Italy'
        WHEN CALLED_NBR LIKE '226%' THEN 'Burkina Faso'
    END AS [Destination Country],
    CASE 
        WHEN CALLED_NBR LIKE '880%' THEN '+880'
        WHEN CALLED_NBR LIKE '86%' THEN '+86'
        WHEN CALLED_NBR LIKE '33%' THEN '+33'
        WHEN CALLED_NBR LIKE '233%' THEN '+233'
        WHEN CALLED_NBR LIKE '224%' THEN '+224'
        WHEN CALLED_NBR LIKE '91%' THEN '+91'
        WHEN CALLED_NBR LIKE '225%' THEN '+225'
        WHEN CALLED_NBR LIKE '961%' THEN '+961'
        WHEN CALLED_NBR LIKE '223%' THEN '+223'
        WHEN CALLED_NBR LIKE '221%' THEN '+221'
        WHEN CALLED_NBR LIKE '232%' THEN '+232'
        WHEN CALLED_NBR LIKE '1%' THEN '+1'
        WHEN CALLED_NBR LIKE '234%' THEN '+234'
        WHEN CALLED_NBR LIKE '44%' THEN '+44'
        WHEN CALLED_NBR LIKE '966%' THEN '+966'
        WHEN CALLED_NBR LIKE '92%' THEN '+92'
        WHEN CALLED_NBR LIKE '351%' THEN '+351'
        WHEN CALLED_NBR LIKE '49%' THEN '+49'
        WHEN CALLED_NBR LIKE '39%' THEN '+39'
        WHEN CALLED_NBR LIKE '226%' THEN '+226'
    END AS [Country Code],
    CustomerType AS [Customer Type],
    COUNT(*) AS [Total Calls],
    SUM(DURATION) AS [Total Duration (Seconds)],
    SUM(CHARGED_AMOUNT) AS [Total Charged Amount],
    MIN(START_TIME) AS [First Call Date],
    MAX(START_TIME) AS [Last Call Date]
FROM [TIMM_Report].[dbo].[xDRVoice]
WHERE START_TIME >= DATEADD(MONTH, -3, GETDATE())
  AND LEN(CALLED_NBR) >= 4
  AND (
    CALLED_NBR LIKE '880%'    -- Bangladesh
    OR CALLED_NBR LIKE '86%'  -- China
    OR CALLED_NBR LIKE '33%'  -- France
    OR CALLED_NBR LIKE '233%' -- Ghana
    OR CALLED_NBR LIKE '224%' -- Guinea
    OR CALLED_NBR LIKE '91%'  -- India
    OR CALLED_NBR LIKE '225%' -- Ivory Coast
    OR CALLED_NBR LIKE '961%' -- Lebanon
    OR CALLED_NBR LIKE '223%' -- Mali
    OR CALLED_NBR LIKE '221%' -- Senegal
    OR CALLED_NBR LIKE '232%' -- Sierra Leone
    OR CALLED_NBR LIKE '1%'   -- USA / Canada
    OR CALLED_NBR LIKE '234%' -- Nigeria
    OR CALLED_NBR LIKE '44%'  -- UK
    OR CALLED_NBR LIKE '966%' -- Saudi Arabia
    OR CALLED_NBR LIKE '92%'  -- Pakistan
    OR CALLED_NBR LIKE '351%' -- Portugal
    OR CALLED_NBR LIKE '49%'  -- Germany
    OR CALLED_NBR LIKE '39%'  -- Italy
    OR CALLED_NBR LIKE '226%' -- Burkina Faso
  )
GROUP BY 
    BILLING_NBR,
    CALLING_NBR,
    CALLED_NBR,
    CustomerType,
    CASE 
        WHEN CALLED_NBR LIKE '880%' THEN 'Bangladesh'
        WHEN CALLED_NBR LIKE '86%' THEN 'China'
        WHEN CALLED_NBR LIKE '33%' THEN 'France'
        WHEN CALLED_NBR LIKE '233%' THEN 'Ghana'
        WHEN CALLED_NBR LIKE '224%' THEN 'Guinea'
        WHEN CALLED_NBR LIKE '91%' THEN 'India'
        WHEN CALLED_NBR LIKE '225%' THEN 'Ivory Coast'
        WHEN CALLED_NBR LIKE '961%' THEN 'Lebanon'
        WHEN CALLED_NBR LIKE '223%' THEN 'Mali'
        WHEN CALLED_NBR LIKE '221%' THEN 'Senegal'
        WHEN CALLED_NBR LIKE '232%' THEN 'Sierra Leone'
        WHEN CALLED_NBR LIKE '1%' THEN 'USA/Canada'
        WHEN CALLED_NBR LIKE '234%' THEN 'Nigeria'
        WHEN CALLED_NBR LIKE '44%' THEN 'UK'
        WHEN CALLED_NBR LIKE '966%' THEN 'Saudi Arabia'
        WHEN CALLED_NBR LIKE '92%' THEN 'Pakistan'
        WHEN CALLED_NBR LIKE '351%' THEN 'Portugal'
        WHEN CALLED_NBR LIKE '49%' THEN 'Germany'
        WHEN CALLED_NBR LIKE '39%' THEN 'Italy'
        WHEN CALLED_NBR LIKE '226%' THEN 'Burkina Faso'
    END,
    CASE 
        WHEN CALLED_NBR LIKE '880%' THEN '+880'
        WHEN CALLED_NBR LIKE '86%' THEN '+86'
        WHEN CALLED_NBR LIKE '33%' THEN '+33'
        WHEN CALLED_NBR LIKE '233%' THEN '+233'
        WHEN CALLED_NBR LIKE '224%' THEN '+224'
        WHEN CALLED_NBR LIKE '91%' THEN '+91'
        WHEN CALLED_NBR LIKE '225%' THEN '+225'
        WHEN CALLED_NBR LIKE '961%' THEN '+961'
        WHEN CALLED_NBR LIKE '223%' THEN '+223'
        WHEN CALLED_NBR LIKE '221%' THEN '+221'
        WHEN CALLED_NBR LIKE '232%' THEN '+232'
        WHEN CALLED_NBR LIKE '1%' THEN '+1'
        WHEN CALLED_NBR LIKE '234%' THEN '+234'
        WHEN CALLED_NBR LIKE '44%' THEN '+44'
        WHEN CALLED_NBR LIKE '966%' THEN '+966'
        WHEN CALLED_NBR LIKE '92%' THEN '+92'
        WHEN CALLED_NBR LIKE '351%' THEN '+351'
        WHEN CALLED_NBR LIKE '49%' THEN '+49'
        WHEN CALLED_NBR LIKE '39%' THEN '+39'
        WHEN CALLED_NBR LIKE '226%' THEN '+226'
    END
ORDER BY [Destination Country], BILLING_NBR;
```

## Filters Applied
- **Time Period:** Last 3 months from current date
- **Called Number Length:** Minimum 4 digits (excludes short codes)
- **Destination:** Only the 21 specified international country codes

## Notes
- USA and Canada share the same country code (+1) and are grouped together
- The query aggregates call data per customer, per called number
- Results are ordered by destination country and billing number

## Author
Bronax N. Barlue

## Version History
| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2025-12-16 | finanl implementation |

