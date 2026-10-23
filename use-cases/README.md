# Use Case Library

Twelve bounded, reusable examples. Every scenario is **illustrative decision support**, not product functionality guaranteed across ChatGPT accounts. Use case claims are: **V** at visualization-format level; **P** for custom dashboards, scores, and control compositions; **K** only if a separately documented ChatKit widget is expressly referenced.

| ID | Domain | Decision-support question |
|---|---|---|
| [UC-01](UC-01-investment-financing.md) | Investment & Project Financing Analyzer | How do capital amount, tenor, scheduled collections, interest/coupon assumptions and fees affect liquidity and investor outcomes? |
| [UC-02](UC-02-investment-committee-sukuk.md) | Sukuk / Investment Committee Scenario Review | Which exposures change under base, downside and severe collection-delay cases? |
| [UC-03](UC-03-financial-health.md) | Financial Health Diagnostic | Are liquidity, leverage and profitability improving or deteriorating? |
| [UC-04](UC-04-saas-metrics.md) | SaaS Conversion, Retention & MRR | Which stage of acquisition, retention or recurring revenue is deteriorating? |
| [UC-05](UC-05-restaurant-workflow.md) | Restaurant Order & Table Session State Simulator | How do table sessions and order-item states transition across dine-in, takeaway and delivery? |
| [UC-06](UC-06-logistics-distribution.md) | Logistics Distribution & Site Reconciliation | Do allocated, delivered and installed unit totals reconcile at each site? |
| [UC-07](UC-07-governance-decision.md) | Governance & Change-Control Workflow | Who may propose, review, authorize, execute and verify a change? |
| [UC-08](UC-08-cap-table-dilution.md) | Cap Table & Dilution Simulator | How do valuation, round size and option-pool assumptions affect fully diluted ownership? |
| [UC-09](UC-09-site-selection.md) | Site Selection Comparison | Which candidate sites best meet access, cost, demand and downside criteria? |
| [UC-10](UC-10-vendor-selection.md) | Vendor Qualification & Trade-off Analysis | Which vendors meet non-negotiable requirements and how do price, lead time and performance trade off? |
| [UC-11](UC-11-interactive-education.md) | Interactive Technical Education Lab | How can changing one physical or mathematical parameter illustrate the underlying mechanism? |
| [UC-12](UC-12-project-cashflow.md) | Project Milestone Cash-Flow Gap | At which milestone does delayed customer collection create a liquidity shortfall? |

## Applying a case

1. Verify the domain data contract and select an allowed source.
2. Adapt the prompt with correct periods, units and control bounds.
3. Reconcile the result to one independent test and inspect missing/invalid inputs.
4. Record product surface and test date, including untested limitations.
5. Treat the result as a non-binding analysis; production actions require a separate system.

**Maintained by:** [Rachmat Efendi](https://rachmatefendi.com). See [rights status](../LICENSE-STATUS.md).
