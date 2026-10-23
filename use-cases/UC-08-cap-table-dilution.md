# UC-08 — Cap Table & Dilution Simulator

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Fundraising / corporate finance  
**Audience:** Founder, CFO or investor  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

How do valuation, round size and option-pool assumptions affect fully diluted ownership?

## 2. Input and data contract

Share classes, holders, outstanding shares, conversion rules, option pool (issued/unissued), pre-money valuation, round size, proposed new shares, exchange and pricing conventions, source version. Define pre- versus post-money pool expansion.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Stacked ownership chart, before/after cap table and dilution sensitivity. Controls: valuation, investment size, pre/post-money option-pool convention. Preserve the same cap table in all views; round only display percentages.

## 4. Copy-ready prompt

```text
@Visualize
Build a hypothetical fundraising dilution calculator from the supplied cap
table. Controls: pre-money valuation, new investment, option pool size and
whether pool expansion occurs pre- or post-money. Show holder-level before/
after fully diluted percentages and a reconciliation to 100%. Distinguish
shares legally issued from purely simulated new allocations; no securities
issuance or corporate approval is represented.
```

## 5. Acceptance tests

- [ ] Each cap table percentage sums to 100% within rounding tolerance.
- [ ] New share count follows the declared price-per-share formula.
- [ ] Pre-money pool expansion dilutes existing holders as specified.
- [ ] All views share one selected financing scenario.
- [ ] Simulated shares are never labeled issued or legally effective.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Conversion terms, preferred share rights, vesting and local corporate law may change actual economics. The model is not corporate or securities advice.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
