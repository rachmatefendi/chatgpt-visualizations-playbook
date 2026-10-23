# Quick Prompt Library

Each prompt is a **design suggestion**. Results depend on surface and available capabilities. Use the linked case for data contracts and acceptance checks.

## Financial performance (UC-03)

```text
@Visualize
Using the attached financial CSV only, plot quarterly revenue, COGS, operating
expenses, gross margin %, and operating cash trends (where supplied). Show units,
source cutoff, filter by quarter and an underlying table. Do not invent missing
ratios or treat this as an audited financial opinion.
```

## Investment financing scenarios (UC-01)

```text
@Visualize
Using my dated, signed cash-flow table, show investor cash flows, financing
balances and an XIRR only when calculable. Expose capital, collection delay and
cost assumptions. Keep shared state across timeline, table and sensitivity view.
Label all scenario inputs hypothetical. This is not financing approval.
```

## Sukuk scenario stress test (UC-02)

```text
@Visualize
Use the attached project and Sukuk source material only. Compare base,
downside and severe delay scenarios using collection timing, haircut and
liquidity coverage. Separate verified, self-reported and unknown data; no
credit rating, Sharia conclusion, guaranteed yield or committee approval.
```

## SaaS metrics (UC-04)

```text
@Visualize
Using the customer-month dataset, build a recurring-revenue trend and cohort
retention view. State cohort eligibility and MRR units; do not invent absent
customer-month records. Share filters across all views and show a source table.
```

## Restaurant workflow explanation (UC-05)

```text
@Visualize
Demonstrate QR table activation, multiple separately paid orders within one
table session, configurable kitchen station routing, item Ready/Served states,
partial dine-in serving, and full-order takeaway/delivery release. Use a state
diagram and transition table. This simulates behavior, not a live POS.
```

## Logistics allocation (UC-06)

```text
@Visualize
Using the provided site CSV, show allocated, delivered and installed units by
site. Map only verified coordinates, list unmapped sites, reconcile unit totals,
and retain the source cutoff. Do not mark delivered as installed or write status
back to a database.
```

## Ownership dilution (UC-08)

```text
@Visualize
Show fully diluted pre- and post-money ownership under illustrative round sizes,
valuations and option-pool assumptions. Reconcile the cap table to 100%, expose
share-count/percentage changes, and avoid claiming any actual issuance occurred.
```

## Educational simulation (UC-11)

```text
@Visualize
Build an interactive model that explains wave interference through wavelength,
source separation and phase controls. Display the governing concepts, a reset
control, accessible text explanation and a small knowledge check. Avoid
presenting a conceptual visualization as measured experiment data.
```
