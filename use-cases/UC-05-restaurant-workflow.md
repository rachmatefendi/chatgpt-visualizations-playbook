# UC-05 — Restaurant Order & Table Session State Simulator

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Restaurant management / workflow design  
**Audience:** Product, kitchen and operations team  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

How do table sessions and order-item states transition across dine-in, takeaway and delivery?

## 2. Input and data contract

Order ID, table session ID, service mode, paid-order boundary, item ID, kitchen station route, kitchen Ready event, Served event, fulfilled event and actor permission assumptions. One row represents an order item; sessions may contain several separately paid orders.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Interactive state diagram, per-item state table and station panels. Model self-activated table session by static QR URL with table reference; partial serving for dine-in; takeaway/delivery released only once every item of that paid order is Ready. Staff close sessions independently of order payment.

## 4. Copy-ready prompt

```text
@Visualize
Explain a restaurant workflow with static table QR short URL, customer
self-activation with validation, multiple separately paid orders per table
session, configurable kitchen station routing, and item-level Ready states.
Dine-in may partially serve Ready items. Takeaway/delivery wait until ALL items
in the paid order are Ready. Show a transition diagram and exception table;
assume no live POS, payment settlement, or actual kitchen dispatch.
```

## 5. Acceptance tests

- [ ] Two paid orders in one table session remain distinct.
- [ ] One Ready dine-in item can be served before others.
- [ ] Takeaway/delivery stays pending while any paid-order item is not Ready.
- [ ] Staff session closure is separate from payment of individual orders.
- [ ] Kitchen routing changes only the configured station assignment.
- [ ] Unpaid or invalid transitions are not silently completed.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

A diagram does not implement QR security, settlement, authorization, concurrency control or real station dispatch. These need separate application requirements and testing.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
