# 2G, 3G, and 4G Customer Base Report - FAQ

## Project Overview

### What is this project?
This project generates a comprehensive report on mobile network customer base and traffic information across different technologies (2G, 3G, and 4G) for a specified time period.

### What data does the report provide?
- **Customer Base Count**: Number of unique customers using each technology (2G, 3G, 4G)
- **Monthly Breakdown**: Customer counts per month and technology
- **Technology Summary**: Total customers across all months per technology
- **Overlap Analysis**: Customers who used multiple technologies during the reporting period

---

## Understanding the Data

### What is "Customer Base with Overlap per Traffic"?
The report counts customers **per technology type**. This means:
- If a customer uses **only 3G** in a month, they appear **once** (in the 3G count)
- If a customer uses **both 3G and 4G** in a month, they appear **twice** (once in 3G, once in 4G)
- If a customer uses **all three technologies** (2G, 3G, 4G), they appear **three times**

**Example:**
```
Customer A uses 3G and 4G in January 2025
- January 3G Count: +1
- January 4G Count: +1
- January Total: Customer A is counted twice
```

### Why does overlap occur?
Modern devices and network conditions can cause users to switch between technologies:
- **Device capabilities**: Smartphones can connect to 2G, 3G, or 4G based on availability
- **Location changes**: Moving between areas with different network coverage
- **Network fallback**: Switching to 2G/3G when 4G signal is weak
- **Manual selection**: Users manually selecting preferred network type

### Is overlap a data error?
**No.** Overlap is **intentional and correct** for this type of analysis. It accurately reflects:
- Customer behavior across multiple technologies
- Network usage patterns
- Technology adoption trends

---

## Technical Details

### What is the data source?
- **Database**: `DMP_GPRS_Repository_202501` (separate database per month)
- **Table**: `GGSNPDPRecord`
- **Key Fields**:
  - `servedMSISDN`: Customer phone number
  - `rATType`: Radio Access Technology type
    - `1` = 3G
    - `2` = 2G
    - `6` = 4G/LTE

### What time period does the report cover?
By default: **January 2025 to October 2025** (configurable)

### How are customers counted?
```sql
COUNT(DISTINCT servedMSISDN)
```
- Each unique phone number (MSISDN) is counted once **per technology**
- The same phone number can appear in multiple technology groups

---

## Using the Report

### What are the three result sets?

**Result Set 1: Monthly Breakdown by Technology**
```
Month    | Technology | Unique Customers
---------|------------|----------------
202501   | 2G         | 45,231
202501   | 3G         | 128,456
202501   | 4G         | 234,789
```

**Result Set 2: Technology Summary**
```
Technology | Total Unique Customers
-----------|----------------------
2G         | 450,000
3G         | 1,200,000
4G         | 2,300,000
```
*Note: Total > actual customer base due to overlap*

**Result Set 3: Monthly Combined Totals**
```
Month  | Total Customers (All Tech)
-------|---------------------------
202501 | 408,476
202502 | 412,893
```
*Note: Includes overlap - same customer counted multiple times if using multiple technologies*

---

## Common Questions

### Q: How do I get the actual unique customer count (no overlap)?
**A:** Use this additional query:
```sql
SELECT COUNT(DISTINCT servedMSISDN) as [Total Unique Customers]
FROM #tmp
```
This counts each customer only once, regardless of how many technologies they used.

### Q: Can I see which customers used multiple technologies?
**A:** Yes, add this query to find multi-technology users:
```sql
SELECT MSISDN, COUNT(DISTINCT Traffic) as [Tech_Count],
       STRING_AGG(Traffic, ', ') as [Technologies_Used]
FROM #tmp
GROUP BY MSISDN
HAVING COUNT(DISTINCT Traffic) > 1
ORDER BY Tech_Count DESC
```
### Q: Why don't you have traffic volume data?
**A:** The `GGSNPDPRecord` table contains customer base information only. Traffic volume data (MB/GB) would need to be sourced from a different table (e.g., `DataUsage`, `TrafficData`, or CDR tables).

### Q: How long does the script take to run?
**A:** Depends on data volume, typically:
- Small dataset (< 1M records): 30 seconds - 2 minutes
- Medium dataset (1-10M records): 2-10 minutes
- Large dataset (> 10M records): 10-30 minutes

---

## Report Interpretation

### Key Insights to Extract

1. **Technology Adoption Trends**
   - Compare customer counts across 2G/3G/4G
   - Track month-over-month growth

2. **Network Migration Patterns**
   - Identify customers moving from 2G → 3G → 4G
   - Measure legacy technology usage

3. **Coverage Analysis**
   - High 2G/3G usage may indicate coverage gaps
   - Multi-technology usage shows network switching behavior

4. **Customer Segmentation**
   - Single-tech users vs. multi-tech users
   - Technology preference by time period

##  Conclusion
    
    This Solution(Report) implements the standardized customer base and traffic analysis methodology for 2G, 3G, and 4G networks within the DMP_GPRS system to maintain consistent, 
    reliable subscriber technology metrics. It ensures the monthly calculation of unique customers per technology, customer overlap across multiple networks, and technology
    adoption patterns are aligned with well-defined telecommunications standards, enabling robust network planning, infrastructure investment decisions, and technology migration strategies
