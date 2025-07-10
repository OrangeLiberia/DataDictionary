# OM.UnifiedCode_GetFeatures Stored Procedure

## Overview

This procedure retrieves unified code details along with each feature’s metadata. When a specific code is supplied, it returns only that record; otherwise, it returns all codes.

---
## Parameters
| Name | Data Type | Description |
|------|-----------|-------------|
| @Code	| VARCHAR(7) | Optional code filter. Returns only the matching record when provided; otherwise, processes all codes. |


## Result Set
| Column | Data Type | Description |
|--------|-----------|-------------|
| MSISDN | VARCHAR(10) | Subscriber number associated with code. |
| Code | VARCHAR(7) | Unified code identifier. |
| Type | VARCHAR(MAX) | Type of Code. |
| TOS  | VARBINARY(MAX) | Type of System. |



## Syntax

```sql
-- Retrieve features for code 'ABC1234'
EXEC OM.UnifiedCodePlan_GetFeatures @Code = '0001234';

-- Retrieve features for all codes
EXEC OM.UnifiedCodePlan_GetFeatures;
