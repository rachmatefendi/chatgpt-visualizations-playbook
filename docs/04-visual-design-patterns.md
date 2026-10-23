# Visual Design Patterns

[← Components](03-ui-components.md) · [Prompting →](05-prompt-engineering.md)

## Pattern library

| Pattern | Use when | Composition | Primary test |
|---|---|---|---|
| Single-view explanation | One relation matters | One chart or diagram + concise context | Reader can state the finding |
| Side-by-side comparison | Alternatives matter | Matched axes, common units, table | Scales and definitions agree |
| KPI snapshot | Fast operational readout | 2–4 metrics + one trend | Every figure reconciles |
| What-if calculator | Output depends on assumptions | Bounded inputs + formula + result | Boundary inputs behave |
| Scenario dashboard | Base/downside/upside comparison | Selector + timeline + sensitivity | Scenario changes propagate |
| Process/state explanation | Transitions and exceptions matter | State diagram + event legend | Impossible transitions are rejected |
| Geographic allocation | Location context is material | Geocoded pins + missing-site list | No fabricated coordinates |
| Teaching lab | Users learn through manipulation | Controls + animation or steps + explanation | Conceptual result remains accurate |

## Layout principles

Lead with the question and output. Keep the primary view dominant, place controls beside or above it, and show the source/period/units below. Put methodological qualifications near the values they constrain, not only in footnotes.

## Avoid false precision

Use visual thresholds only where the threshold has a documented source. Confidence bands, risk ranks, and traffic-light badges can mislead if they imply scientific or regulatory certainty. Mark scores as **illustrative** when hypothetical.

## Multi-view handoff

When a layout needs a calculator, cash-flow timeline, scenario table and heatmap, specify a **shared state contract** before requesting rendering. Refer to [Data and State](06-interactivity-and-data.md) for invariants and cross-view tests.
