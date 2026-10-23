# Playbook 03 — From Data Source to Dashboard

**Objective:** Build an analytical dashboard without mixing data definitions, forecasts, and missing values.

## Procedure

1. Determine dataset ownership, intended use, confidentiality and personal-data constraints.
2. Inspect **grain**: does a row represent an item, paid order, table session, customer-month or site? Deduplicate at the proper key.
3. Define each metric: numerator, denominator, reporting period, unit, source, timestamp and scope of eligible rows.
4. Profile nulls, duplicate IDs, missing periods, currencies, outliers and cases where 0 ≠ unknown.
5. Select up to three questions: trend, driver and exception.
6. Request one main chart, supporting KPI/filter controls, and a table of underlying values.
7. Reconcile totals and ratios to independent calculations from the raw file.
8. Switch one filter and verify every dependent view shares the same state.
9. Disclose snapshot date and missing data; never claim real-time unless separately connected and validated.

## Three illustrative metric definitions

| Metric | Formula | Grain | Caution |
|---|---|---|---|
| Gross margin % | `(revenue - COGS) / revenue × 100` | Period | Undefined when revenue = 0 |
| Order fulfillment rate | `fulfilled eligible paid orders / all eligible paid orders` | Paid order | Item ready ≠ entire order fulfilled |
| Lead conversion | `converted unique eligible leads / eligible unique leads` | Cohort | Cohort windows must match |

**Escalate** to application engineering for persistent users, recurring refresh, audit logs, complex entitlements or live operational actions.
