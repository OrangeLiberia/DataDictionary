# OM.UnifiedCode_Cancel Stored Procedure

## Overview

This stored procedure cancels a unified code by moving it from the active plan to history. It performs validation, status update, archival insertion, and deletion within a single transaction to ensure data consistency.

---
## Parameters
Name	Data Type	Description
@Code	VARCHAR(7)	The unique identifier of the unified code to cancel.

## Return Value
Returns an integer representing the number of rows deleted from OM.UnifiedCode. A return value of zero indicates that no matching code was found or deleted.


## Error Handling
If the code is not found in OM.UnifiedCodePlan, the procedure raises error 51003 with the message “Code not found in Plan.”

SET XACT_ABORT ON ensures that any runtime error triggers an automatic rollback of the transaction.


## Syntax

```sql
DECLARE @DeletedCount INT;

EXEC @DeletedCount = OM.UnifiedCode_Cancel
  @Code = 'ABC1234';

PRINT 'Deleted rows: ' + CAST(@DeletedCount AS VARCHAR(3));