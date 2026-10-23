# Limitations, Security, Privacy & Authority

[← QA](07-accessibility-and-qa.md) · [Product Boundaries →](09-chatkit-vs-visualize.md)

## Key boundaries

**A visualization is not a source of authority.** The presence of a score, status, warning color, “Approved” button or workflow diagram does not prove an investment was approved, a payment completed, a vendor certified, a halal/Sharia opinion issued, or a legal requirement satisfied.

**A snapshot is not a live integration.** Unless a live data source and its freshness are explicitly confirmed, treat the result as a static analysis of the available material. The official guide cautions that shared visualizations are generally snapshots.

**One test is not universal support.** UI generation can vary by account, model, platform, permissions and rollout. Repeat tests on the intended surface.

## Data-handling checklist

- Use only information the organization is permitted to share and process.
- Minimize personal, financial and sensitive records; anonymize or synthesize wherever possible.
- Validate source links, amounts and inputs; do not insert secret credentials into prompts.
- Review the **entire chat**, not only the visual, before sharing.
- Use explicit source cutoff, scenario vs actual classification, and document provenance.
- For real actions, enforce authentication, authorization, logging and server-side validation outside the visualization.

## Finance and regulatory use cases

Models are educational and analytical only: no guaranteed returns, formal investment recommendation, securities offering, legal opinion, Sharia determination, tax advice or binding approval. Indonesia-specific references to IDR, Sukuk and local project contexts are examples, not endorsements or determinations of compliance.

## Escalation trigger

When the proposed experience requires a database, authorization decisions, customer-specific data entitlements, audit logs, repeated unattended computation, regulated advice or financial transactions, stop describing it as a chat visualization and initiate a separate product/security specification.
