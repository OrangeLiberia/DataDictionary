# Orange Energy Subscription FAQ

This FAQ provides guidance on how to interpret and query the **[DMP_Generic_Repository].[OSE].[SubscriptionStatusChanges]** table for Orange Energy subscriptions.

---

## What does the `SubscriptionStatusChanges` table contain?
The table records **all status changes** for each subscription over time.  
Each row represents a change event with details such as:
- `subscriptionId` – unique identifier of the subscription
- `changeType` – type of status change (e.g., installation, creation, fee payment)
- `changeDate` – timestamp of when the change occurred
- `changeAgent` – user or system responsible for the change

---

## Why does the same `subscriptionId` appear multiple times?
A subscription can go through **several lifecycle stages** (installation, approval, payment, repossession, etc.).  
Therefore, the same `subscriptionId` will appear multiple times, each with a different `changeType` and `changeDate`.

---

## How can I identify the subscription state after installation?

To determine the subscription state after installation:
1. Filter the table by the relevant `subscriptionId`.
2. Order the results by `changeDate` in ascending order.
3. Locate the row where `changeType = 'installation'`.
4. The **next row(s)** represent the state transitions that follow installation.

### 📌 Example: Subscription ID 1001129

| changeType             | changeDate           | changeAgent |
|------------------------|----------------------|-------------|
| creation               | 2022-09-29 17:27     | mjonjo      |
| feePayment             | 2022-09-30 15:54     | NULL        |
| approval               | 2022-09-30 15:56     | ckouassi    |
| uninstallation         | 2022-10-03 16:12     | jbrown      |
| installation           | 2022-11-28 17:15     | jbrown      |
| requireRepossession    | 2022-11-28 17:15     | jbrown      |
| repossession           | 2022-11-28 17:15     | jbrown      |

In this case:
- The subscription was **installed** on 2022-11-28.
- Immediately after, it entered a **repossession flow**, indicating a failed or reversed activation.

---

## How do I track monthly subscriptions for end users?
- Use the **sequence of change events** to reconstruct the subscription timeline.
- Identify the **installation event** as the starting point.
- Subsequent events (e.g., `feePayment`, `approval`) indicate ongoing monthly activity.
- Group by `subscriptionId` and filter by `changeType` values relevant to billing.

---

## Which filters are most useful for analysis?
- `changeType = 'installation'` → marks the subscription start.
- `changeType = 'feePayment'` → indicates monthly subscription activity.
- `changeType = 'approval'` → confirms activation.
- `changeType = 'repossession'` or `changeType = 'requireRepossession'` → marks failure or reversal.
- `changeType = 'uninstallation'` → indicates service removal.

---

## Best practices for querying
- Always **order by `changeDate`** to maintain chronological accuracy.
- Use **specific `subscriptionId` filters** to analyze individual subscriptions.
- For bulk analysis, aggregate by `subscriptionId` and `changeType`.

**Example Query:**
```sql
SELECT *
FROM [DMP_Generic_Repository].[OSE].[SubscriptionStatusChanges]
WHERE subscriptionId = 1001129
ORDER BY changeDate ASC;