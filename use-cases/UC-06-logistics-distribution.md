# UC-06 — Logistics Distribution & Site Reconciliation

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Logistics / site allocation  
**Audience:** Operations and deployment manager  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Do allocated, delivered and installed unit totals reconcile at each site?

## 2. Input and data contract

Site ID, verified site coordinate/address, allocation group, destination, item ID, allocated units, shipment confirmation, installed confirmation and event date. Preserve one record per defined site/asset grain and distinct allocation/delivery/installation states.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Pin map (verified coordinates only), region/status filters, reconciliation scorecard, exception table for unmatched site/unit records. Illustrative sample allows two units per site; blank coordinates are unmapped, not geocoded automatically.

## 4. Copy-ready prompt

```text
@Visualize
Using only the supplied logistics site file, map verified coordinates, show
allocated, delivered and installed totals by site, and list unmapped sites
separately. Controls: region and operational status; all totals and map filters
must be consistent. Reconcile units and record the report cutoff. Do not invent
sites/coordinates, mark delivered as installed, or write back to a live system.
```

## 5. Acceptance tests

- [ ] Allocated units reconcile to source site/unit counts.
- [ ] A delivered item is not automatically installed.
- [ ] Missing coordinate leaves a site in the exception table.
- [ ] Region filter changes pin set and matching totals.
- [ ] Repeated assets are deduplicated only by declared keys.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

Map pins are synthetic test positions, not evidence of actual delivery sites. No inventory or vendor authorization is implied.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
