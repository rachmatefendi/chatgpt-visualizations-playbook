# Visualizations vs ChatKit vs Hosted Applications

[← Limitations](08-limitations-security.md) · [Decision Guide →](10-decision-guide.md)

| Capability | ChatGPT Visualizations | ChatKit widgets | Hosted application / Site |
|---|---|---|---|
| Primary purpose | Explore concepts/data in a chat | Embed developer-defined UI in a chat experience | Durable product experience |
| Format / documented layer | Visual formats and interactive examples | Named developer-facing widgets | Application implementation and hosting |
| Data updates | Usually snapshot; verify source scope | Depends on implementation | Can implement refresh and persistence |
| Identity/permissions | Chat account and workspace context | Host/application integration | Explicitly designed authentication/roles |
| Guaranteed public renderer API | **Not claimed here** | **ChatKit docs apply to ChatKit** | Depends on chosen stack |
| External side effects | Not implied by visual controls | Only via explicitly wired actions | Via authenticated backend |

**Do not** label ChatKit Select or Form as an official `@Visualize` SDK component. The fact that a similar control can be rendered does not establish shared APIs or compatibility.

## Routing test

If the need is **show me and let me explore this question once**, start with Visualizations. If it is **deliver structured embedded UI to app users**, evaluate ChatKit. If it is **operate a secure, repeated, persistent workflow**, design an application with a backend. There can be overlap in user experience, but not automatic interchangeability of capabilities.

## Migration handoff

Carry forward the decision question, datasets, data-contract definitions, verified formulas, UX behaviors, test vectors and identified risk boundaries. Rewrite authentication, persistence, error handling, auditability, security and integration as explicit product requirements.
