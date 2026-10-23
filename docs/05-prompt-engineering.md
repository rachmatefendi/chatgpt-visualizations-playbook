# Prompt Engineering Playbook

[← Patterns](04-visual-design-patterns.md) · [Data & State →](06-interactivity-and-data.md)

## The O–S–Q–F–C–A–V prompt contract

1. **Outcome:** what the user wants to understand or decide.
2. **Source:** allowed records, time period, data owner and freshness.
3. **Question:** one primary analytical question and dimensions.
4. **Format:** chart, diagram, map, calculator, simulation or explanation.
5. **Controls:** editable inputs with type, default, limits, and dependencies.
6. **Assumptions:** formulas, units, missing data policy, dates, rounding and scenario conventions.
7. **Verification:** test vectors, table fallback, accessibility, and prohibited claims.

## Copy-ready master prompt

```text
@Visualize
OUTCOME: [Decision or learning outcome.]
SOURCE: [Supplied file/table/authorized connected source, period, unit and source date.]
Do not invent missing observations, addresses, benchmarks, or verification status.
QUESTION: [Primary comparison, metric, and dimensions.]
FORMAT: [Smallest suitable chart/diagram/map/calculator/simulation.]
CONTROLS: [Name, type, default, range, step, and views impacted.]
LOGIC: [Formula, unit conversion, calendar/timezone, filter and rounding rules.]
OUTPUT: [Main visual, concise summary, source/assumption labels, tabular fallback.]
VERIFY: [Known test case, boundary case, empty state, cross-view consistency.]
ACCESSIBILITY: Keyboard navigation, focus visibility, text labels, reduced motion.
BOUNDARIES: Analysis only; not a live feed, binding approval, or external transaction.
```

## Iterative refinement sequence

1. Request one visual and at most two essential controls.
2. Inspect labels, units, formulas, and default results.
3. Add only the drill-down or scenario control necessary for the decision.
4. Verify accessibility, missing-data handling, negative values, and edge conditions.
5. Escalate to application planning for database persistence, authentication, API integration or real approval workflows.

## Two worked anti-pattern repairs

### Anti-pattern A — The impressive but ungrounded finance dashboard

**Weak prompt:** “Build a beautiful, complete investment dashboard and show my ROI.”

**Likely bad result:** Attractive graphs with arbitrary input figures, an undefined ROI formula, a selected yield treated as a guaranteed return, or a visual badge implying the financing is approved.

**Better prompt:**

```text
@Visualize
Use ONLY the attached dated cash-flow rows (negative investment outflows,
positive investor inflows). Show capital at risk by date and an XIRR result only
when dated cash flows support it. Define the convention, show the underlying
cash-flow table, and label all unknown tax/cost assumptions as unavailable.
Provide base and 90-day-delay scenarios, with all scenario values labeled
hypothetical. Never display "approved", "compliant", or "guaranteed return".
Check the default result against an independent spreadsheet computation.
```

**Required improvement:** Provenance, formula definition, testable scenario mechanics, uncertainty disclosure, no implied authority.

### Anti-pattern B — An apparently live operations map

**Weak prompt:** “Map all our deliveries, update everything live, and mark missing sites delivered.”

**Likely bad result:** Guessed locations, a map that looks current without an authenticated live feed, and delivery state silently inferred from incomplete data.

**Better prompt:**

```text
@Visualize
Use only the supplied site IDs, addresses or coordinates and event timestamps.
Show mapped sites and a separate unmapped count; never guess coordinates.
Calculate allocated, delivered and installed units as distinct states at the
source cutoff timestamp. Expose region and status filters, list records with
missing location or status evidence, and label this a static snapshot.
No ERP/database writeback or operational status mutation is authorized.
```

**Required improvement:** Location integrity, explicit snapshot timestamp, stage separation, no unauthorized writeback.

## Further anti-patterns

| Avoid | Replace with |
|---|---|
| “Make the most complete dashboard” | Define audience, one question, and minimum view |
| “Show yield” | Supply dated cash flows, calculation conventions and costs |
| “Map every address” with no addresses | Require verified locators and surface unmapped records |
| “Just make it accurate” | Provide sample inputs with independently checkable expected outputs |
| “Connect directly to my ERP” | Specify a separate integration and authorization project |
| “Refresh in real time” | Distinguish an analytical snapshot from a verified live pipeline |

For domain-specific prompts see [Quick Prompts](../prompts/quick-start.md) and [12 Use Cases](../use-cases/README.md).
