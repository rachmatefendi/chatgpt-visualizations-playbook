# Getting Started

[← README](../README.md) · [Evidence & Scope →](01-scope-and-evidence.md)

## The five-minute path

1. Identify the decision question (for example: “Where does cash coverage turn negative if collections slip by three months?”).
2. Check the source: permitted data, grain, dates, completeness, units, and verified versus reported attributes.
3. Choose a diagram, chart, map, calculator, simulation, or explanation. Avoid a whole dashboard if one chart suffices.
4. Ask for specific controls and an underlying table. Use [the core prompt](../templates/prompt-base.md).
5. Interact, verify one normal case and one edge case, then record a decision-support result with its limitations.

## Accessing Visualizations

If available in your ChatGPT composer, type `@`, search for **Visualize** under Plugins, and select it. Availability varies by plan, platform, account and workspace; do not infer eligibility solely from this guide.

## Your first prompt

```text
@Visualize
Explain gross margin movement using the attached CSV.
Show quarterly revenue, COGS, and gross margin %. Include a quarter selector,
units (IDR million), an underlying data table, and a two-sentence summary.
Do not infer missing quarters. Validate margin as (revenue - COGS) / revenue.
This is an analytical snapshot, not a live financial system.
```

Use [synthetic-financial-performance.csv](../examples/data/synthetic-financial-performance.csv) for practice, then complete the [QA checklist](../templates/acceptance-checklist.md).
