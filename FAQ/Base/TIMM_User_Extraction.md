# 📊 TIMM User Extraction Report – FAQ

## 📌 Overview

This document explains the SQL query used to extract TIMM user accounts created between **January 1, 2026 and June 3, 2026**, including account status, password information, creator details, and last login activity.

---

##  What is the purpose of this report?

This report provides a list of TIMM user accounts created within a specified period and includes:

- User login name
- Full name
- Account creation date
- Password change date
- Account status (Active/Inactive)
- Account creator
- Last login date
- Associated account description

The report supports:

- 👤 User account audits
- 🔒 Security reviews
- 📊 Access management reporting
- 🛡️ Compliance and governance checks

---

##  What systems are used in this query?

The query retrieves data from:

| Database | Table | Purpose |
|-----------|---------|---------|
| TIMM_ADMIN | AdminAccount | User account information |
| TIMM_ADMIN | AdminAccountGroup | User group assignments |
| TIMM_LOG | LogApplication_2024 | User login history |

---

##  What date range is used?

The report includes users created between:

```sql
'2026-01-01' AND '2026-06-03'
```

This filter is applied using:

```sql
DataCriacao BETWEEN '2026-01-01' AND '2026-06-03'
```

---

##  Which users are excluded?

The query excludes users belonging to Group ID:

```sql
10189
```

Filter used:

```sql
WHERE IDGroup != 10189
```

This ensures users from that specific group are not included in the report.

---

##  How is account status determined?

The query translates the `Desactivado` field into a readable status.

```sql
CASE
    WHEN [Desactivado] = 0 THEN 'Active'
    ELSE 'Inactive'
END
```

### Status Mapping

| Desactivado Value | Status |
|------------------|---------|
| 0 | Active |
| 1 | Inactive |

---

##  What information is captured?

### Initial User Extraction

The first query captures:

| Field | Description |
|---------|-------------|
| Login | User account name |
| Fullname | User description/full name |
| Creation Date | Date account was created |
| Password Change Date | Last password update |
| Status | Active or Inactive |
| Created By | User who created the account |
| Last Login Date | Most recent login activity |
| IDAccount | Internal account identifier |

---

##  How is the last login date calculated?

The query retrieves the latest login record using:

```sql
MAX([created_at])
```

This returns the most recent login activity found in the log table.

---

##  Why is a temporary table used?

The query stores the initial results in:

```sql
#users
```

Benefits:

- Improves readability
- Simplifies reporting
- Avoids repeating complex joins
- Makes further filtering easier

---

##  What happens in the second query?

The second query joins the temporary table back to the account table:

```sql
SELECT u.Login,
       u.Fullname,
       u.[Creation Date],
       u.[Password Change date],
       u.status,
       a.Description
```

This retrieves additional descriptive information associated with each account.

---

##  What fields are returned in the final report?

| Field | Description |
|---------|-------------|
| Login | Username |
| Fullname | Full user name |
| Creation Date | Account creation date |
| Password Change Date | Last password update |
| Status | Active/Inactive |
| Description | Account description |

---

##  How is the report sorted?

### First Query

```sql
ORDER BY 2
```

Sorts by:

```text
Fullname
```

### Final Query

```sql
ORDER BY 1 DESC
```

Sorts by:

```text
Login (Descending)
```

---

##  What are common use cases for this report?

### User Administration

- Review newly created accounts
- Identify inactive users
- Verify account ownership

### Security Audits

- Review password age
- Monitor login activity
- Detect dormant accounts

### Compliance Reviews

- Track account creation
- Verify account lifecycle management
- Support internal audits

---

##  Full SQL Script

```sql
DROP TABLE #users;

SELECT
    Account [Login],
    Description [Fullname],
    CONVERT(Date, DataCriacao) [Creation Date],
    CONVERT(Date, DataPassword) [Password Change date],
    CASE
        WHEN [Desactivado] = 0 THEN 'Active'
        ELSE 'Inactive'
    END AS [status],
    LastUserID [Created by],
    MAX([created_at]) [Last login date],
    a.[IDAccount]
INTO #users
FROM [TIMM_ADMIN].[dbo].[AdminAccountGroup] a
INNER JOIN [TIMM_ADMIN].[dbo].[AdminAccount] b
    ON a.IDAccount = b.IDAccount
LEFT JOIN [TIMM_LOG].[dbo].[LogApplication_2024] l
    ON a.IDAccount = l.IDAccount
WHERE IDGroup != 10189
  AND DataCriacao BETWEEN '2026-01-01' AND '2026-06-03'
GROUP BY
    Account,
    Description,
    DataCriacao,
    DataPassword,
    Desactivado,
    LastUserID,
    a.[IDAccount]
ORDER BY 2;

SELECT
    u.Login,
    u.Fullname,
    u.[Creation Date],
    u.[Password Change date],
    u.status,
    a.Description
FROM [TIMM_ADMIN].[dbo].[AdminAccount] a
INNER JOIN #users u
    ON a.IDAccount = u.[IDAccount]
ORDER BY 1 DESC;
```

---

##  Summary

This report:

- Extracts TIMM users created between January and June 2026
- Identifies active and inactive accounts
- Captures password update history
- Retrieves the latest login activity
- Supports user administration, security auditing, and compliance reporting

---

## 👨‍💻 Author

**James Anointed Morgan Jr.**  
MIS Engineer
