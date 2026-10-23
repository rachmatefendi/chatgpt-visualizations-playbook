# UC-04 — SaaS Conversion, Retention & MRR

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** SaaS / subscription analytics  
**Audience:** Product and growth leader  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Which stage of acquisition, retention or recurring revenue is deteriorating?

## 2. Input and data contract

Cohort/customer-month records, pseudonymous customer ID, eligibility definitions, activity flag, plan, monthly recurring revenue, cancellations and reporting date. Define when a customer is counted and whether missing months represent absence or missing data.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

MRR trend, conversion funnel, cohort retention matrix (design pattern) and metric table. Controls: cohort, segment and period. Consistent filter scope and denominators; never conflate churned customers with missing records.

## 4. Copy-ready prompt

```text
@Visualize
Using the provided customer-month data, show MRR by month and retention by
signup cohort. Make cohort eligibility and retention denominator explicit.
Controls: cohort range and segment; share filters across KPI, chart and table.
Use IDR-thousand units from the source and distinguish no-record from zero MRR.
Do not invent customer events or causal attribution.
```

## 5. Acceptance tests

- [ ] MRR equals sum of eligible customer-month amounts.
- [ ] Retention denominator stays fixed to the initial eligible cohort.
- [ ] Segment filter propagates to all visible views.
- [ ] Missing customer-months are not silently treated as observed churn.
- [ ] Display all conversion formula definitions.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Attribution, seasonality and cohort bias can create false growth diagnoses. Synthetic sample records are not real revenue results.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
