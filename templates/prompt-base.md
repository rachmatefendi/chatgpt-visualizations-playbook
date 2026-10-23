# Universal Prompt Template

```text
@Visualize
OUTCOME: Explain [decision question] for [audience].
DATA: Use only [authorized attached file/table], cutoff [date], grain [record unit],
currency/unit [specified]. Flag missing, hypothetical and unverified fields.
VISUAL: Produce [one primary format] with [optional essential supporting view].
CONTROLS: [parameter; type; default; min/max; step; dependent views].
FORMULAS: [precise definitions, day-count/compounding, missing value policy].
STATE: Share [selected scenario, filters, date range and currency] across all views.
OUTPUT: Clear labels/units, concise result, underlying table and assumptions.
TEST: Validate [known fixture], boundary [edge], reset, empty case and cross-view sync.
ACCESSIBILITY: Keyboard, visible focus, textual alternative and reduced motion.
AUTHORITY: Analytical demo only; no live sync, database writeback or approval claim.
```

For practice, use [synthetic datasets](../examples/data/README.md). If `@Visualize` is unavailable, request an accessible static chart/table and explicitly mark interaction as not tested.
