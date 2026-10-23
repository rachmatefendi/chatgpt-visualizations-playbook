# UI Component Inventory (Evidence-Labeled)

[← Capabilities](02-capability-matrix.md) · [Patterns →](04-visual-design-patterns.md)

**Important:** This is a cross-surface *inventory*, **not an `@Visualize` component API reference**. A “K” component is documented for ChatKit, not necessarily available as a public Visualizations primitive. A “P” item is a candidate interaction/design pattern, not a product guarantee.

| Family | Elements (representative) | Typical use | Evidence |
|---|---|---|---|
| Core formats | chart, diagram, map, calculator, simulation, interactive explanation | Understanding, comparisons, what-if | V |
| Input/actions | button, editable text, select, date picker, form | Capture/filter/submit in documented ChatKit | K |
| Display & layout | card, badge, box, row, col, list view, text, title, caption, icon, image, divider, spacer, markdown | Readable result composition | K |
| Interactive patterns | slider, checkbox, radio group, segmented control, textarea, search, popover, modal | Parameter selection and disclosure | P |
| Information patterns | table, progress, carousel, heatmap, sankey, treemap, gauge, network graph | Multiple views or specialist charts | P |
| Workflow patterns | Kanban, file upload pathway | Stateful applications and connected actions | P |

**Clarification:** Controls resembling sliders may appear in official Visualizations demos, but the guide does not establish a separately supported public slider component API. Likewise, an “upload” control must not be assumed to support file ingestion in a given visualization.

See the full [43-row CSV inventory](../catalog/component-evidence.csv) with source basis and recommended use.

## Interaction design guidelines

- Label each input with unit, default, valid range and what it changes.
- On a filter change, update *all dependent views* or visibly state which view is unaffected.
- Distinguish action verbs: **Preview / Simulate / Export / Submit**. A “Submit” prototype must not imply real external execution.
- Show empty, loading, invalid, and no-data states.
- Avoid color as the only signal; provide text and a table where calculation traceability matters.

## Example composition

A financing analysis may use a **Select** concept for scenario, a **Slider** *pattern* for delay, and a **Chart** format for cash coverage. Whether a particular runtime can generate all of these must be tested rather than assumed.
