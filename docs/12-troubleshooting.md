# Troubleshooting

[← Maintenance](11-publishing-and-maintenance.md) · [References →](references.md)

| Symptom | Likely issue | Practical recovery |
|---|---|---|
| `@Visualize` not shown | Account/platform rollout or settings | Check supported surface; consult official availability documentation |
| Blank or partial output | Rendering complexity or interrupted generation | Retry once; reduce controls, rows, precision or animation |
| Widget appears but does not update | Unsupported/failed interaction binding | Ask for a simpler control and verify the affected state |
| Chart and table disagree | Filter, unit or model-state mismatch | Return to a single source + deterministic calculation |
| Scenario silently invents values | Missing data contract | Force explicit assumptions, missing value status and source references |
| Timeline date shifted | Timezone/calendar mismatch | Specify source timezone, WIB/UTC convention and date boundaries |
| “Download” does not work | Generated export varies by result | Request a plain table or supported export separately |
| Map contains suspicious locations | Geocoding guess or ambiguous names | Supply verified addresses/coordinates; report unmapped separately |
| Approval button looks actionable | Confusing prototype with workflow | Rename to “Preview” or “Simulate”; no real side-effect claim |
| Shared result looks current when stale | Snapshot mistaken for live dashboard | Show creation date, data cutoff, and source |

## Minimal recovery prompt

```text
Please rebuild the visualization using only the attached data.
Remove unsupported controls and animations. Keep one primary chart,
clear units, a source cutoff date, and an underlying verification table.
Do not create missing data. Explain any functionality that cannot be
implemented or tested on this ChatGPT surface.
```

Verify the new result against data; a replacement visualization may not modify the previous artifact in place. See [official troubleshooting guidance](https://learn.chatgpt.com/docs/visualizations).
