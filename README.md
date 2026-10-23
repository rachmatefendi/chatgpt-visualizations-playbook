# ChatGPT Visualizations Playbook

> **A practical, evidence-aware guide to interactive visualizations, UI patterns, prompt design, validation, and real-world use cases.**

**Created and curated by [Rachmat Efendi](https://rachmatefendi.com)**  
**Edition:** 1.0.0 (English) · **Documentation checked:** 2026-10-23 · **Live behavior last spot-checked:** Not yet performed

[Getting Started](docs/00-start-here.md) · [UI Components](docs/03-ui-components.md) · [Playbooks](playbooks/01-discovery-to-prototype.md) · [Use Cases](use-cases/README.md) · [Prompt Library](prompts/quick-start.md)

> [!IMPORTANT]
> **Independent community documentation, not an OpenAI publication or SDK.** ChatGPT Visualizations, the developer-facing ChatKit widget system, and custom UI patterns are **different products or design layers**. A feature demonstrated here is not a guarantee that every user, plan, renderer, or account supports it.

## Why this repository exists

Visual interfaces can make complex relationships easier to explore, but a convincing widget is not proof that the underlying data, math, permissions, or decision is correct. This repository provides a repeatable workflow for going from **decision question → data contract → visualization → verification → responsible use**.

**Who it is for:** product managers, founders, analysts, developers, educators, operations teams, and decision-support practitioners. **It is documentation and reusable prompts—not a production application, embedded component SDK, regulated advisory service, or authorization engine.**

## Scope at a glance

| Layer | Meaning | Examples | Evidence tier |
|---|---|---|---|
| ChatGPT Visualizations | Formats described in official Visualizations documentation | Charts, diagrams, maps, calculators, simulations, interactive explanations | **V** |
| ChatKit Widgets | Separately documented developer components | Card, Button, Select, DatePicker, Form, layout primitives | **K** |
| Custom UI design patterns | Proposed compositions, not guaranteed native components | Risk heatmap, timeline, Kanban, sensitivity grid, wizard | **P** |

**V/K/P is about the source of the claim, not quality or product maturity.** See [Evidence & Boundaries](docs/01-scope-and-evidence.md) and [43-item Component Catalog](catalog/component-evidence.csv).

## Quick start (5 minutes)

1. Check whether `@Visualize` appears under **Plugins** in your ChatGPT composer. Availability depends on your account, platform, and rollout.
2. Define the *one question* a visualization should answer. Use the [Decision Guide](docs/10-decision-guide.md) to choose the smallest suitable format.
3. Supply source data, units, periods, assumptions, and desired interactions using the [Prompt Template](templates/prompt-base.md) or [Ready-to-Use Prompts](prompts/quick-start.md).
4. Inspect the result and test edge cases with the [Acceptance Checklist](templates/acceptance-checklist.md). Reconcile calculations against the input data.
5. If you need persistence, authentication, or backend actions, plan an application separately. The interactive chat artifact is not a production system.

## Repository guide

| Start here | What you will find |
|---|---|
| [Scope & Evidence](docs/01-scope-and-evidence.md) | Distinguish documented behavior from prototype patterns |
| [Capability Matrix](docs/02-capability-matrix.md) | Select charts, maps, diagrams, simulations, or calculators |
| [UI Components](docs/03-ui-components.md) | 43 categorized elements with V/K/P evidence labels |
| [Visual Design Patterns](docs/04-visual-design-patterns.md) | Single-view, comparison, scenarios, and decision-support layouts |
| [Prompt Engineering](docs/05-prompt-engineering.md) | Prompt formula and concrete anti-pattern repairs |
| [Data Contracts & State](docs/06-interactivity-and-data.md) | Units, formulas, shared state, and multi-view consistency |
| [Accessibility & QA](docs/07-accessibility-and-qa.md) | Functional, numerical, and inclusive validation |
| [Security & Limitations](docs/08-limitations-security.md) | Data sensitivity, authority and snapshot boundaries |
| [ChatKit vs Visualize](docs/09-chatkit-vs-visualize.md) | Decide between a chat visualization and a hosted product |
| [Decision Guide](docs/10-decision-guide.md) | Practical visualization choice matrix |
| [Publishing & Maintenance](docs/11-publishing-and-maintenance.md) | Change triggers, owners and stale-content markers |
| [Troubleshooting](docs/12-troubleshooting.md) | Recovery paths when controls or graphics fail |
| [Operational Playbooks](playbooks/01-discovery-to-prototype.md) | Five repeatable procedures |
| [12 Use Cases](use-cases/README.md) | Decision question, input contract, prompt, tests, limits |
| [Synthetic CSVs](examples/data/README.md) | Five fictional datasets to practice reconciliation |
| [References](docs/references.md) | Official sources and verification status |

## Guiding principles

- **Smallest sufficient visualization:** choose one useful view before adding dashboard complexity.
- **Source integrity:** never invent actuals, benchmarks, geographic coordinates, or verified status.
- **Deterministic checks:** verify important calculations independently; distinguish assumptions from source records.
- **Snapshot ≠ live feed:** a chat visualization is generally a snapshot unless a live integration is separately established.
- **UI ≠ authority:** showing an “Approve” control does not authorize funds, issue securities, complete compliance, or approve decisions.
- **Shared-state consistency:** filters, periods, currencies, and scenario assumptions must agree across calculator, timeline, chart, and table.
- **Accessibility:** provide labels, units, keyboard operation, and a tabular/text fallback.

## Example applications

**Investment and corporate finance:** financing scenario models, cash-flow gap visualization, dilution models, committee analysis (no investment decision delegation). **Business operations:** SaaS KPIs, restaurant order-state explanation, vendor comparisons, logistics allocation. **Technology and governance:** workflow/state diagrams, dependency explanation, education labs, and prototype design review.

See the [Use Case Index](use-cases/README.md) for twelve fully scoped examples. Example financial values are **synthetic**, denominated in **IDR** where specified, and not investment advice or regulatory conclusions.

## Verification and change status

| Verification dimension | Status as of 2026-10-23 |
|---|---|
| Reference documents | Reviewed against published documentation |
| Markdown links, CSV structure, repository package | Passed local structural QA on 2026-10-23 (46 Markdown files; 43 catalog rows; 5 CSV fixtures) |
| Live ChatGPT Visualizations interactions | **Not yet spot-checked** across user accounts and product surfaces |
| Production integration / backend capability | **Not implemented or claimed** |

See [CHANGELOG](CHANGELOG.md), [Maintenance Policy](docs/11-publishing-and-maintenance.md), and [Source Registry](docs/references.md). Revalidation is triggered by relevant documentation changes or OpenAI release notes, not by assuming a static feature list.

## Licensing and publication

**Copyright © 2026 Rachmat Efendi. All rights reserved unless and until an explicit license is selected.**

The package intentionally includes **no open-source/open-content license**. Public visibility on GitHub does not automatically grant reproduction or derivative-work rights. Do not describe the repository as MIT-, CC BY-, or otherwise open-licensed. See [LICENSE-STATUS.md](LICENSE-STATUS.md).

## Attribution and independence

**Created and curated by Rachmat Efendi** — [https://rachmatefendi.com](https://rachmatefendi.com).  
This is an independent educational project and is **not affiliated with, sponsored by, or endorsed by OpenAI**. Product and company names remain the property of their respective owners. See [NOTICE](NOTICE.md).

## Primary source links

- [OpenAI ChatGPT Visualizations documentation](https://learn.chatgpt.com/docs/visualizations)
- [OpenAI ChatKit widget documentation](https://developers.openai.com/api/docs/guides/chatkit-widgets)
- [ChatGPT release notes](https://help.openai.com/en/articles/6825453-chatgpt-release-notes)

**Repository name:** `chatgpt-visualizations-playbook` · **Suggested GitHub owner:** `rachmatefendi` · **Publication default:** private pending licensing decision.
