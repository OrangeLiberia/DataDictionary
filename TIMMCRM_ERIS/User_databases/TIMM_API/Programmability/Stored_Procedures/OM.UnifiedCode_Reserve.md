# OM.UnifiedCode_Reserve Stored Procedure

## Overview

This procedure reserves a specified number of unified codes from the plan. It validates inputs, selects available codes with locking hints to avoid conflicts, marks them as reserved, and returns the reserved codes in a result set.

---
## Parameters
| Name | Data Type | Description |
|------------|------------|------------|
|@Quantity | INT | Number of codes to reserve; must be greater than zero. |
|@Type | VARCHAR(8) | Optional plan type filter (Platinum, Golden, Silver, Normal). Normal is the default value|



## Return Value
### Result Set
On success, the procedure returns one row per reserved code with the following columns:


| Column	| Data Type |	Description
|------------|------------|------------|
|Code	| VARCHAR(7) | Unique code identifier reserved. |
|Type	| INT |	Internal numeric plan type. |
|NameType	| VARCHAR(8) | Human-readable plan type name. |

## Error Handling
Throws 51000 if:
    @Quantity is less than or equal to zero.
    @Type is not one of the recognized values

Throws 51011 if insufficient free codes are available to fulfill the reservation.

XACT_ABORT ON guarantees a full rollback upon any runtime error.


## Syntax

```sql
-- Reserve 5 codes of type 'Silver'
EXEC OM.UnifiedCodePlan_Reserve
  @Quantity = 5,
  @Type     = 'Silver';
