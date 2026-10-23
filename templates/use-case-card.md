# Use Case Template — UC-XX: [Title]

**Domain:** [Sector]  
**Audience:** [User role]  
**Evidence classification:** V (format); K (ChatKit-only named widget if relevant); P (custom pattern).

## 1. Decision question

[What should the user understand? What does not get decided?]

## 2. Input and data contract

[Data fields, units, grain, dates, source, verified/reported/scenario classification.]

## 3. Visualization design

[Primary view, secondary view, controls, default state, expected dependencies, calculation model.]

## 4. Copy-ready prompt

```text
@Visualize
[Outcome, exact source, controls, logic, validation and boundaries.]
```

## 5. Acceptance tests

1. [Source reconciliation]
2. [Deterministic normal case]
3. [One edge/missingness case]
4. [Shared control-state behavior]
5. [No authority/side-effect claim]

Record PASS / FAIL / NOT TESTED with surface and date.

## 6. Risks and prohibited claims

[Domain-specific misleading states, security concerns and limits.]

## 7. Handoff boundary

[Chat prototype versus secure persistent application responsibilities.]
