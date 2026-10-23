# UC-12 — Project Milestone Cash-Flow Gap

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Project finance / delivery operations  
**Audience:** Project owner or lender analyst  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

At which milestone does delayed customer collection create a liquidity shortfall?

## 2. Input and data contract

Milestone IDs, planned versus actual dates, budget/spend curve, invoice dates, payment terms, dated customer collections, financing drawdowns, opening cash, currency and source status. Distinguish contract claims from bank-confirmed receipts.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Milestone timeline, cumulative cash-balance chart and downside scenario table. Controls: collection delay, cost overrun, date filter and financing draw date. Show lowest cash balance and shortfall by date under each scenario.

## 4. Copy-ready prompt

```text
@Visualize
Using only the supplied project milestone and cash-flow records, show a dated
milestone timeline and cumulative cash balance with optional delay and cost
stress. Controls: collection delay months and cost-overrun percentage; keep
selected scenario and IDR units synchronized across views. Highlight any
negative cash position without inventing credit lines or actual receipts.
Show a reconciliation table and source cutoff.
```

## 5. Acceptance tests

- [ ] Opening cash plus signed inflows/outflows equals closing cash.
- [ ] Collection delay changes dates without increasing forecast revenue.
- [ ] Higher cost overrun never improves modelled cash position ceteris paribus.
- [ ] Missing invoice or receipt date is flagged.
- [ ] Scenario table and chart show identical liquidity minimum.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Cash gap illustrations are not a funding commitment, credit approval or verification of payment collection. Operational execution needs auditable finance systems.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
