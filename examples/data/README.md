# Synthetic Example Datasets

**All records are fictional training fixtures.** Any coordinates, IDs, times, amounts, businesses, and outcomes in these files are **not evidence of real projects, customer activity, investments or deliveries**. Even when coordinates point to a real geographic area, they are synthetic marker positions and not real operational sites.

| File | Grain | Data dictionary / verification |
|---|---|---|
| [synthetic-financial-performance.csv](synthetic-financial-performance.csv) | one quarter | `revenue_idr_million`, `cogs_idr_million`, `operating_expense_idr_million` are numeric in IDR million; gross margin = `(revenue-cogs)/revenue` |
| [synthetic-project-cashflows.csv](synthetic-project-cashflows.csv) | one investor cash-flow event | negative disbursement; positive coupons/principal; example only, not sukuk terms or guaranteed yield |
| [synthetic-rms-items.csv](synthetic-rms-items.csv) | one order item | session can have >1 paid order; `Ready` is not equal to `Served`; for takeaway/delivery, fulfillment awaits all ready |
| [synthetic-saas-cohorts.csv](synthetic-saas-cohorts.csv) | one customer-month | pseudonymous demo IDs, `active_flag` is 0/1, `mrr_idr_thousand` in IDR thousand; missing customer-months not present |
| [synthetic-logistics-sites.csv](synthetic-logistics-sites.csv) | one synthetic site | demo lat/long; 2 allocated units per site; blank coordinate demonstrates unmapped site; installed is not synonymous with delivered |

## Use

1. Attach one CSV to a ChatGPT conversation.
2. Select `@Visualize` if available and paste the matching domain prompt from [use cases](../../use-cases/README.md).
3. Validate row counts and totals against the CSV; use [acceptance checklist](../../templates/acceptance-checklist.md).
4. Do **not** claim these are live, real, audited, or actual customer records.

## Guardrails

Currencies use only illustrative magnitudes; no inflation, exchange-rate, or tax assumptions have been supplied. Rounding and period conventions must be declared by the generated model. No sensitive personal information is included.
