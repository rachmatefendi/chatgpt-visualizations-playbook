# UC-02 — Sukuk / Investment Committee Scenario Review

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Sukuk, capital markets, investment assessment  
**Audience:** Committee support analyst  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Which exposures change under base, downside and severe collection-delay cases?

## 2. Input and data contract

Project budget, financing requested, dated forecast collections, payment schedule, issuer/counterparty dependencies, guarantee/security representations, source citations and verification status. Separate reported, verified and unknown fields.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Scenario matrix, cumulative liquidity timeline and cash-flow waterfall, with optional risk-return conceptual plot. Controls: collection delay, realization haircut, recovery assumption explicitly flagged as hypothetical. Keep probability separate from severity; do not generate ratings or Sharia determinations.

## 4. Copy-ready prompt

```text
@Visualize
Build an interactive investment committee scenario review using ONLY the
attached Sukuk and project data. Compare base, downside and severe delay for
cash coverage, liquidity gap and payment dates. Controls: collection delay,
realization haircut, hypothetical recovery %. Mark data verified/reported/
unknown, show source references and a scenario-delta table. Never assert a
credit rating, Sharia compliance, guaranteed coupon or actual committee approval.
```

## 5. Acceptance tests

- [ ] Base scenario reconciles to project records.
- [ ] Delay shifts dates without creating revenue.
- [ ] Realization haircut reduces collections.
- [ ] Unknown collateral valuation remains unknown/N/A.
- [ ] Any benchmark is accompanied by source and date.
- [ ] No button or badge implies actual approval.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

This is committee decision support, not a legal, Sharia, investment, issuer-rating or regulatory opinion. Credit and collateral recovery remain uncertain and require independent due diligence.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
