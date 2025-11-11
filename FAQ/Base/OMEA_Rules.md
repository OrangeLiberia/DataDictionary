# Subscriber Activity and Churn Rules (AMEA, Orange Group)

This document summarizes the key telecom subscriber activity and churn calculation rules that are implemented by the stored procedure `[dbo].[spc_ProcessActiveSubsBasePyramidDaily]`. The rules reflect Orange Group standards for counting, measuring, and analyzing churn in mobile markets across the AMEA region.

## 1. Gross Adds (New Mobile Customer Acquisitions)

- A **gross add** is counted when a new customer is connected to the network and is authorized to make outgoing or receive incoming voice or non-voice calls.
- The customer does **not** need to actually make a call or event; being authorized (e.g., after SIM activation) is sufficient.
- This definition helps track "dead on arrival" customers who never generate activity.
- Applies to prepaid and postpaid mobile handsets and broadband devices.
- Excludes M2M, MVNO, and fixed broadband customers.

## 2. Orange Closing Base (Active Subscriber Base)

- Includes both prepaid and postpaid customers deemed **active**.
- Prepaid customers are active if they made at least **1 outbound chargeable event** or **4 inbound chargeable events** in the last 90 days.
- A **chargeable event** includes any event with a direct/indirect contractual charge: calls (voice & non-voice), SMS, MMS, data sessions, and downloads (ringtones, games, logos).
- Initial credits, bundles, or bonuses also count as chargeable events.
- Orange Money transactions except Cash In count as outbound chargeable events.
- Excludes specific non-chargeable events such as customer service calls, marketing SMS, USSD sessions (except those ending with purchase), account top-ups (except OM top-ups), bundle purchases, and rate plan subscriptions.
- Disconnections include voluntary terminations, portability outs, and forced disconnections for bad debt (postpaid).
- New customers who do not meet the activity threshold are not included in the closing base but classified as acquisition churn.
- The **charged base** is a subset of the closing base, representing customers with at least one outgoing chargeable event during the month.
- The **IN base** or **registered base** includes all customers registered on the network, active or not.

## 3. Churn Rate Calculations

### 3.1 Monthly Churn Rate

\[
\text{Monthly Churn Rate} = \frac{\text{Disconnections of the Month}}{\text{Average Closing Base}}
\]

- Disconnections calculated as:  
  \[
  \text{Disconnections} = \text{Opening Base} + \text{Gross Adds} - \text{Closing Base}
  \]
- Average closing base is the average of the opening base and closing base for the month.

### 3.2 Annualized Monthly Churn Rate

- Monthly churn rate multiplied by 12 to extrapolate for a full year.

### 3.3 Year-to-Date (YtD) Churn Rate

\[
\text{YtD Churn Rate} = \frac{\text{Cumulated Disconnections since January}}{\text{Average of average closing bases since January}} \times \frac{12}{\text{Number of months to date}}
\]

- Resets every calendar year.
- Smooths out seasonal/exceptional variations.
- More reliable as it accounts for possible counting corrections.

## 4. Split of Disconnections by Tenure

Disconnections are classified to better understand churn origins and target actions:

- **Acquisition Churn**  
  Disconnections of customers with tenure up to **1 month**. Indicates fake acquisitions or "dead on arrival" customers.

- **Gratuity Churn**  
  Disconnections with tenure between **3 and 5 months**. Reflects opportunistic customers exploiting offers or dissatisfied new customers.

- **Structural Churn**  
  Disconnections with tenure of **6 months or more**. Represents core churn due to network issues, customer service, market conditions, portability, etc.

Additional categories (seasonal, regulatory, multi-SIM) exist for detailed analysis but are beyond the main churn KPIs.

## Notes

- Tenure is calculated from the gross add (registration) date, not from first inclusion in the closing base.
- Reconnection customers (inactive then reactivated) are accounted for in churn calculations to avoid inflating disconnections.
- The definitions aim to standardize KPIs such as gross adds, churn rates, closing bases, and charged bases across the AMEA region.
- Local affiliate or regulatory definitions might differ.

---

This churn framework matches the KPI calculations and subscriber activity logic coded in the stored procedure, ensuring coherent and standardized reporting for business intelligence and operational decisions.
