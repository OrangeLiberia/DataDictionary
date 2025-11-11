# Stored Procedure Summary: spc_ProcessActiveSubsBasePyramidDaily

The stored procedure `[dbo].[spc_ProcessActiveSubsBasePyramidDaily]` calculates and updates key daily and monthly subscriber KPIs for a telecom business intelligence database, implementing churn and activity rules based on Orange Group standards for the AMEA region (as per July 2015 memorandum).

It aggregates active subscriber activities, new registrations, disconnections, churn metrics, and more, then updates summary tables with these derived values.

## Core Functionality

This procedure:
- Determines the date range for analysis (defaults to previous day if not specified).
- Executes main logic covering three-month historical context to compute subscriber status and churn metrics.
- Creates temporary tables aggregating subscriber activities: outbound/inbound calls & SMS, data usage, value-added services (VAS), roaming, and Orange Money events.
- Applies standardized business rules for activity classification and churn definition.
- Calculates monthly and year-to-date churn rates along with detailed churn segmentation by subscriber tenure.
- Updates key summary tables reflecting subscriber base and churn KPIs.

## Key Business Rules Applied (from AMEA Churn Framework)

### Subscriber Activity and Base Inclusion Criteria

- **Active Subscriber Definition:**  
  A prepaid or postpaid customer is considered active if in the last 90 days they have at least 1 outbound chargeable event or 4 inbound chargeable events.  
- **Chargeable Events:** Includes voice and non-voice calls, SMS, MMS, data sessions, downloads, bundle usage, and Orange Money transactions (excluding cash-in).  
- **Non-Chargeable Events Excluded:** Customer care calls, marketing SMS, USSD sessions (except those leading to purchases), account top-ups (except Orange Money top-ups), and bundle purchases or plan subscriptions.  
- **Closing Base:** Active subscribers as per above criteria at the month end.  
- **Charged Base:** Subset of the closing base with at least one outgoing chargeable event during the month.  
- **IN Base (Registered Base):** All subscribers registered on the network, including inactive ones.

### Gross Adds (New Subscriber Acquisitions)

- Registered customers authorized to use network services (voice or non-voice).  
- Authorization (SIM activation) is enough; actual call activity not required.  
- Captures "dead on arrival" customers who never become active.

## Monthly KPI Calculation Overview

- Aggregates subscriber events and activity from usage and transactional tables.  
- Determines active status combining calls, SMS, data, VAS, roaming, and Orange Money activity.  
- Inserts data into `ActiveSubsBaseMonthly` and aggregates to `ActiveSubsBasePyramidMonthly`.  
- Updates metrics like gross adds, closing/opening base, disconnections, reconnections, net adds, and churn subcategories.

## Churn Metrics and Classification

### Calculations

- **Monthly Churn Rate:**  
  \[
  \text{Churn Rate} = \frac{\text{Disconnections of the Month}}{\text{Average Closing Base}}
  \]  
  where  
  \[
  \text{Disconnections} = \text{Opening Base} + \text{Gross Adds} - \text{Closing Base}
  \]

- **Annualized Churn Rate:** Monthly churn multiplied by 12.

- **Year-to-Date (YtD) Churn Rate:**  
  \[
  \frac{\text{Cumulated Disconnections}}{\text{Average of Average Closing Bases}}\times \frac{12}{\text{Months elapsed}}
  \]

### Disconnection Classification by Subscriber Tenure

- **Acquisition Churn:** Tenure ≤ 1 month (fake acquisitions or immediate disconnections).  
- **Gratuity Churn:** Tenure 3 to 5 months (opportunistic use or dissatisfaction phase).  
- **Structural Churn:** Tenure ≥ 6 months (core market churn due to network/service factors).  

### Additional Churn Considerations

- Customers classified as reconnected if they return after inactivity.  
- Fake acquisitions identified by missing recharge or bundle purchase post-registration.  
- Churn KPIs are updated reflecting these granular classifications to enable targeted actions.

## Detailed KPI Summary Table

| KPI Name                         | Description                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| NSubsActive                     | Number of active subscribers                                                 |
| NSubsMOCalls/MOSMS/HData/VAS/etc| Various activity metrics (calls, SMS, data, VAS, roaming, money, etc.)       |
| KPIGrossAdd                    | Number of valid new subscriber registrations (gross adds)                    |
| KPIClosingBase/KPIOpeningBase   | Subscribers present at close/open of month                                   |
| KPIAverageClosingBase            | Average of closing base over period                                          |
| KPIChargedBase                 | Count of currently charged subscribers                                       |
| KPITotalBase                  | Total base as per core service tables                                        |
| KPIDisconnection/KPINetAdd      | Mathematical and event-based subscriber disconnections/net additions         |
| KPIReconnection               | Subscribers returning after absence                                          |
| KPITotalDisconnections        | Aggregate of disconnections and reconnections                                |
| KPITotalDisconnectionsChurn   | Number of subscribers leaving ("churn")                                      |
| KPIAcquisionChurn/Gratuity/Structural Churn | Churn subcategories based on tenure and origin                     |
| KPIFakeAcquision              | Registrations with no recharge or bundle buy                                 |
| KPIMonthlyChurnRate/Annualized | Churn percentage metrics (monthly/annualized)                                |
| KPIYtDChurnRate               | Year-to-date churn rate                                                      |

## Conclusion

This procedure implements the standardized [Orange Group AMEA](OMEA_Rules.md) churn methodology within the BI system to maintain consistent, reliable subscriber metrics. It ensures the monthly calculation of active base, churn types, gross adds, and churn rates are aligned with well-defined industry and corporate standards, enabling robust operational and marketing analysis and decision-making.
