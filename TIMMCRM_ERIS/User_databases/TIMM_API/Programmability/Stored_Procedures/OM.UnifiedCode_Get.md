# OM.UnifiedCode_Get Stored Procedure

## Overview

This procedure retrieves unified code records from the OM.UnifiedCode table. When a specific code is supplied, it returns that single record; if no code is provided (NULL), it returns all available records.

---
## Parameters
| Name | Data Type | Description |
|------|-----------|-------------|
| @Code	| VARCHAR(7) | Optional code filter. Returns only the matching record when provided; otherwise, processes all codes. |


## Result Set
| Column | Data Type | Description |
|--------|-----------|-------------|
| Currency | VARCHAR(8) | Transaction currency code. |
| MSISDN | VARCHAR(10) | Associated mobile subscriber number. |
| Code | VARCHAR(7) | Unified code identifier. |
| Name | VARCHAR(256) | Descriptive name of the code. |
| Logo | VARBINARY(MAX) | Binary data for the code’s logo. |


## Error Handling
This procedure does not explicitly throw errors.

Invalid inputs (e.g., overly long @Code) will result in normal SQL Server validation errors.


## Syntax

```sql
-- Retrieve a single code
EXEC OM.UnifiedCodePlan_Get @Code = 'ABC1234';

-- Retrieve all codes
EXEC OM.UnifiedCodePlan_Get;
