# Scope, Terminology & Evidence Discipline

[← Getting Started](00-start-here.md) · [Capability Matrix →](02-capability-matrix.md)

## What Visualizations means

[OpenAI's Visualizations documentation](https://learn.chatgpt.com/docs/visualizations) describes interactive charts, maps, diagrams, calculators, simulations, and explanations in a ChatGPT conversation. The preview and individual experiences can vary by plan, workspace, platform and rollout.

## Three evidence tiers

| Tier | Source of claim | What can be stated | What cannot be inferred |
|---|---|---|---|
| **V** | Official ChatGPT Visualizations documentation | Supported visualization *formats* and documented behavior | A stable public renderer/component API for every control |
| **K** | Official ChatKit developer documentation | Names and documented capabilities of ChatKit widgets | Automatic availability of a ChatKit component inside `@Visualize` |
| **P** | Repository design recommendation or illustrative pattern | Feasible pattern to prototype, test or develop independently | An officially supported native widget or guaranteed runtime behavior |

V/K/P describes **evidence provenance**, not product maturity or desirability. For inventory see [the component catalog](03-ui-components.md).

## Outside this repository's scope

This is not an SDK, developer API, private DIL renderer guide, official technical specification, persistent application, compliance engine, live brokerage UI, payment system, or investment advisory service. A text prompt does not guarantee external data access, authentication, storage or side effects.

## Published availability, reviewed 2026-10-23

| Surface | Documentation-derived description |
|---|---|
| ChatGPT web | Available on supported accounts in Chat and ChatGPT Work |
| ChatGPT desktop | Rolling out as a preview |
| ChatGPT mobile | Rolling out to eligible accounts; controls may differ |
| Codex CLI/IDE | Does not render Visualizations |

Check the official page before relying on these statements for deployment. **Live behavior not independently spot-checked for this edition.**

## Evidence logging

Use four independent statuses: **published documentation**, **source-derived claim**, **locally tested behavior**, and **unverified assumption**. Never promote a design illustration or a successful prompt on one platform into a universal compatibility guarantee.
