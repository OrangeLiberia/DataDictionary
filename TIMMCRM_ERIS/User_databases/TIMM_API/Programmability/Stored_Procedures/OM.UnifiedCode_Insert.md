# OM.UnifiedCode_Insert Stored Procedure

## Overview

This procedure adds a new unified code to the plan, enforcing business rules on status, type, and terms of service. It archives any previously canceled entry, constructs feature metadata, and inserts the fresh record in a single transactional scope.

---
## Parameters
| Name | Data Type | Description |
|------------|------------|------------|
|@Code | VARCHAR(7) | Unique identifier for the unified code. |
|@MSISDN | VARCHAR(10) | Mobile subscriber number associated with the code. |
|@Name | VARCHAR(256) | Descriptive name of the code. |
|@Type | VARCHAR(32) | Code category; allowed values: MERCHCODE, CASHOUT. |
|@TOS | VARCHAR(32) | Terms of service tag; allowed value: MERCH. |
|@Status | TINYINT | Initial status; must be 5 (Reserved) or 10 (Active). |
|@Currency | VARCHAR(8) | Optional currency code for transactions. |
|@Logo | VARBINARY(MAX) | Optional binary data for the code’s logo. |



## Return Value
Returns an integer indicating the number of rows inserted into the plan table. A zero return suggests no insertion occurred (typically due to a duplicate prevention check).


## Error Handling
Throws 51000 if:
    @Status is not 5 or 10
    @Type is not MERCHCODE or CASHOUT
    @TOS is not MERCH

Throws 51001 if the code already exists in an active or reserved state.

XACT_ABORT ON guarantees a full rollback upon any runtime error.


## Syntax

```sql
DECLARE @InsertedCount INT;

EXEC @InsertedCount = OM.UnifiedCode_Insert
  @Code     = 'XYZ1234',
  @MSISDN   = '1234567890',
  @Name     = 'Test Merchant Code',
  @Type     = 'MERCHCODE',
  @TOS      = 'MERCH',
  @Status   = 10,
  @Currency = 'USD';

PRINT 'Rows inserted: ' + CAST(@InsertedCount AS VARCHAR(3));
