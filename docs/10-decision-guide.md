# Visualization Decision Guide

[← Product Comparison](09-chatkit-vs-visualize.md) · [Publishing →](11-publishing-and-maintenance.md)

## Choose by analytical question

| Question | First choice | Supporting element | Avoid |
|---|---|---|---|
| What moved over time? | Line chart | Summary table | 3D trend distortion |
| Which category leads? | Sorted bar chart | Unit and denominator | Pie with dozens of slices |
| How are factors related? | Scatter | Definitions/outliers | Causal claims from correlation |
| How does financing react to assumptions? | Calculator + one sensitivity view | Formula and dated cash flows | Hidden defaults, false precision |
| How do tasks progress? | Workflow/state diagram | Transition table | Diagram represented as backend enforcement |
| Where are assets? | Map | Unmapped locations table | Guessing site coordinates |
| What changes with physical parameters? | Simulation | Equation and controls | Motion without meaningful learning |
| How do we understand a sequence? | Interactive explanation | Step labels, reset | Decorative animation |

## Decision checklist

- Is geographic/spatial context essential? If yes, map.
- Does the user need to change inputs? If yes, calculator/simulation with bounded controls.
- Are dependencies or statuses central? If yes, diagram and transition rules.
- Is the question numeric and static? If yes, chart or table.
- Does correctness require a second view? If yes, add a table or only one secondary chart.

Never choose a complex UI purely because more components are available. If the user needs persistent records, user accounts, subscriptions, approvals or integration, select a production development route rather than a chat-only prototype.
