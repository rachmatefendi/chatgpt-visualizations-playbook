# UC-03 — Financial Health Diagnostic

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Corporate finance / accounting  
**Audience:** Finance manager or advisor  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Are liquidity, leverage and profitability improving or deteriorating?

## 2. Input and data contract

Periodic statements with reporting currency, accounting period, source version, revenue, COGS, operating expenses, cash, payables, receivables, debt, current assets and current liabilities where available. Identify unaudited/self-reported inputs.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

KPI cards, ratio trends and source table. Controls: entity, period and metric group. Define ratio formula and denominator; do not infer ratios from missing balance sheet fields. Use the financial sample dataset for gross margin demonstrations.

## 4. Copy-ready prompt

```text
@Visualize
Using only the attached financial tables, calculate gross margin, expense
ratio and other liquidity/leverage ratios only where numerator and denominator
are present. Show trends by reporting period and a table with formulas, units
and source dates. Controls: period and metric. Differentiate missing/zero and
actual/estimated. Do not characterize the result as an audit opinion.
```

## 5. Acceptance tests

- [ ] Gross margin matches (revenue−COGS)/revenue.
- [ ] Zero revenue yields undefined margin, not zero percent.
- [ ] Period filter changes KPI, chart and table together.
- [ ] Missing balance sheet ratios display N/A.
- [ ] Report currency and audited/unaudited provenance clearly.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

A diagnostic score is not a credit rating, audit, certification or regulatory conclusion. Accounting-period changes and inconsistent definitions may invalidate comparisons.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
