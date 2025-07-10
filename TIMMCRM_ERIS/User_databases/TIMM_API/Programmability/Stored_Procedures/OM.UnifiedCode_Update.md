# OM.UnifiedCode_Update Stored Procedure

## Overview

This procedure updates one or more optional attributes of an existing unified code record. It uses a null-coalescing pattern to only overwrite columns when a corresponding input parameter is supplied. If no matching code is found, it raises an error.

---
## Parameters
| Name | Data Type | Description |
|------------|------------|------------|
| @Code	| VARCHAR(7) | Mandatory code identifier of the record to update. |
| @MSISDN |	VARCHAR(10) = NULL | New mobile subscriber number; leaves unchanged when NULL. |
| @Name |	VARCHAR(256)= NULL | New descriptive name; leaves unchanged when NULL. |
| @Type |	VARCHAR(32) = NULL | New category type; leaves unchanged when NULL. |
| @TOS | VARCHAR(32) = NULL | New Terms of Service tag; leaves unchanged when NULL. |
| @Currency | VARCHAR(8) = NULL | New currency code; leaves unchanged when NULL. |
| @Logo | VARBINARY(MAX)=NULL | New binary logo data; leaves unchanged when NULL. |



## Error Handling
51002: Thrown when no record matches the supplied @Code.

No transaction or retry logic is present, so all updates occur in autocommit mode.

XACT_ABORT ON guarantees a full rollback upon any runtime error.


## Syntax

```sql
-- Update Name and Currency on code 'ABC1234'
EXEC OM.UnifiedCodePlan_Update
  @Code     = '0001234',
  @Name     = 'New Display Name';
