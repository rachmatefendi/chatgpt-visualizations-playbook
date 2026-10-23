# UC-09 — Site Selection Comparison

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Location intelligence / investment planning  
**Audience:** Operations, property or investment team  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Which candidate sites best meet access, cost, demand and downside criteria?

## 2. Input and data contract

Verified candidate addresses/coordinates, area/access costs, rent assumptions, operating expenses, demand estimates, footfall source and timing, risk factors, decision constraints and sources. Missing location or demand evidence must remain explicit.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Candidate pin map, side-by-side table and optional weighted-scoring scenario. Controls: hard constraints and illustrative weights. Source/assumption columns reveal where scoring is judgmental rather than measured.

## 4. Copy-ready prompt

```text
@Visualize
Compare candidate sites from the supplied addresses and cost/demand table.
Use verified coordinates only; list any sites that cannot be located. Show
rent, access, demand assumption, risks and missing evidence. Let the user
adjust disclosed illustrative weights but never present a weighted score as a
verified market valuation or final lease/investment authorization.
```

## 5. Acceptance tests

- [ ] Candidate list exactly matches supplied sites.
- [ ] Ungeocodable records are reported, not invented.
- [ ] Rent units/periods are aligned before comparison.
- [ ] Changing weights changes ranking but not raw observations.
- [ ] All hard constraints are shown before subjective rankings.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Demand forecasts, traffic assumptions, legal zoning and due diligence must be separately verified; a map-based recommendation is provisional.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
