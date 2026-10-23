# Visualization Capability Matrix

[← Evidence](01-scope-and-evidence.md) · [UI Elements →](03-ui-components.md)

| Format | Best decision question | Typical input | Useful interaction | Common failure | Tier |
|---|---|---|---|---|---|
| Chart / plot | What changed? What is correlated? | Time series, categories, metrics | Period selector, series filter, hover | Distorted baseline or invented records | V |
| Diagram | What connects, depends, or transitions? | States, actors, steps, edges | Branch explanation, step navigation | A flowchart mistaken for enforced workflow | V |
| Map | Where are objects or routes? | Verified addresses or coordinates | Pin selection, layer filter | Guessed geocoding or route metrics | V |
| Calculator | How does an output vary with inputs? | Formula and bounded values | Slider, number entry, reset | Incorrect units / hidden assumptions | V |
| Simulation | What happens if assumptions change? | Model, initial state, controls | Scenario/parameter switching | Assumptions represented as observed reality | V |
| Interactive explanation | How does a mechanism work? | Steps and teaching concept | Reveal, experiment, replay | Attractive but inaccurate analogy | V |

**Selection rule:** choose the smallest form that communicates the insight. Add secondary charts or tables only if they answer a separate, defined question. A table is often necessary as a *verification fallback*, regardless of the primary visual.

## Composite patterns

A calculator + timeline + sensitivity matrix is useful when all three refer to the **same** model state. Establish a single time basis, currency, filter, scenario and calculation specification; verify each view against a common example. See [Shared-State Consistency](06-interactivity-and-data.md#multi-view-state-consistency).

## Escalation boundary

Use a separate hosted application specification when you require persistent records, granular permissions, recurring live refresh, auditable approval, or external side-effecting operations. Chat visualization does not substitute for these controls.
