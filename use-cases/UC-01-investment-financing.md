# UC-01 — Investment & Project Financing Analyzer

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Project finance / capital allocation  
**Audience:** Founder, investor or analyst  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

How do capital amount, tenor, scheduled collections, interest/coupon assumptions and fees affect liquidity and investor outcomes?

## 2. Input and data contract

Dated positive/negative cash flows, principal, funding date, currency (IDR million where relevant), contractual terms, fees, taxes, collection schedule, source date and evidence status. Separate **issuer/project cash** from **investor cash**; both must not be conflated.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Investor return calculator with dated cash-flow timeline and balance table. Optional sensitivity grid for stressed collections only after baseline formula verification. Controls: initial investment, tenor, delay months, collection haircut and fee assumptions. Preserve dates and signs; XIRR only when there are sufficient signed, dated entries.

## 4. Copy-ready prompt

```text
@Visualize
Analyze ONLY the supplied financing cash-flow records. Show the financing
balance timeline, principal outstanding and investor return using XIRR only if
dated signed flows permit it. Controls: funded principal, collection delay,
collection haircut and fees. Keep all views synchronized to the selected
scenario. Show the underlying dated cash-flow table and explicit IDR units.
Unknown taxes/collateral values are N/A. No financing approval or promise of yield.
```

## 5. Acceptance tests

- [ ] Base totals reconcile to the supplied cash-flow file.
- [ ] A three-month delay shifts collection dates but creates no new cash.
- [ ] A haircut lowers collections and cash coverage in the affected scenario.
- [ ] XIRR is withheld when signed/date data are insufficient.
- [ ] All values use declared currency and timing conventions.
- [ ] Neither investor approval nor contractual certainty is implied.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Return calculations can be distorted by signs, dates, reinvestment assumptions or mixing entity-level and investor-level cash flows. Scenario returns are not guaranteed investor outcomes.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
