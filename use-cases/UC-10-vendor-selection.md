# UC-10 — Vendor Qualification & Trade-off Analysis

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Procurement / project management  
**Audience:** Procurement or project lead  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Which vendors meet non-negotiable requirements and how do price, lead time and performance trade off?

## 2. Input and data contract

Vendor IDs, bid price/currency, lead time, mandatory requirements, historical performance source, risk disclosures, comparable scope, tax treatment and bid date. Avoid hidden preferences and inferred certifications.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Eligibility gate table, cost vs delivery-time scatter and optional illustrative weighted ranking. Controls: minimum mandatory requirement and weight sliders. Failures at hard gates remain ineligible regardless of weighted score.

## 4. Copy-ready prompt

```text
@Visualize
Use only the supplied vendor proposals and requirement matrix. First label
which mandatory conditions each bid satisfies; then compare eligible vendors
on normalized price, lead time and historical delivery metrics. Offer scenario
weights with an explicit formula and show results in a table. Do not invent
certifications, supplier performance, formal qualification or award approval.
```

## 5. Acceptance tests

- [ ] Mandatory gates are evaluated before weighted scores.
- [ ] Unit/currency equivalence is verified for comparable bids.
- [ ] Changing weight changes score, not eligibility gate.
- [ ] Unknown performance shows N/A instead of an assumed score.
- [ ] No UI badge constitutes formal supplier selection.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Bid scope differences, concentration risk and contract enforceability can outweigh simple scores. Final procurement decisions require authorized review.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
