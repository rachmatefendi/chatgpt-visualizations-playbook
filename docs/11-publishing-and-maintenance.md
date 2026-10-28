# Publishing, Change Monitoring & Maintenance

[← Decision Guide](10-decision-guide.md) · [Troubleshooting →](12-troubleshooting.md)

## Publication checklist

1. Confirm repository owner, chosen visibility and **licensing status**.
2. Review the latest OpenAI Visualizations documentation and ChatKit docs independently; update the evidence table.
3. Verify all examples are synthetic or cleared for publication; check that no passwords, customer records, or confidential material are included.
4. Run Markdown link validation, CSV integrity checks, and independent numerical fixtures.
5. Inspect README render, relative links, Mermaid, sample prompts, and GitHub issue templates.
6. Record docs review date and **live spot-check date separately** (including NOT TESTED).
7. Retain author attribution, rights notice and no-affiliation disclaimer.
8. Publish to the deliberately selected repository; confirm remote URL and default branch before claiming success.
9. Record tag/release only once remote repository contents and release artifact have been verified.

## Change-monitoring triggers

| Trigger | Owner | Action |
|---|---|---|
| OpenAI release notes mention **Visualizations** or a product-surface change | Repository maintainer / Rachmat Efendi | Check product page; inspect tier V and availability sections |
| [Visualizations documentation](https://learn.chatgpt.com/docs/visualizations) materially changes | Repository maintainer | Compare behavior examples; flag impacted pages |
| [ChatKit widget docs](https://developers.openai.com/api/docs/guides/chatkit-widgets) change | Repository maintainer | Recheck tier K names; never automatically relabel as V |
| Verified live behavior contradicts documentation | Tester + maintainer | Record surface and reproduction; mark claim **UNDER REVIEW** |
| Community issue includes sourced, reproducible correction | Maintainer | Targeted validation and scoped documentation patch |

**Cadence:** event-driven on meaningful updates; a scheduled quarterly source sweep is a recommendation, not an automated process included in this repo.

## Staleness and status protocol

Add this notice at the top of any affected section until evidence is resolved:

```markdown
> **STATUS: REVIEW REQUIRED** — This section may be outdated due to
> [source change/event, YYYY-MM-DD]. Last docs check: YYYY-MM-DD.
> Last live spot-check: NOT TESTED (or YYYY-MM-DD, surface).
```

Record a separate issue with source URL, scope, evidence tier, observed contradiction, date, reproduction steps and proposed delta. Do not silently update a tier or expand capabilities. Possible states: **CURRENT**, **REVIEW REQUIRED**, **DEPRECATED**, **NOT LIVE-TESTED**.

## Versioning

- **MAJOR:** evidence framework or fundamental audience/scope changed.
- **MINOR:** new domain playbooks, use cases or significant guidance.
- **PATCH:** sourced correction, clarity fix or broken link repair.

## Suggested GitHub metadata

- Name: `chatgpt-visualizations-playbook`
- Description: `Independent guide to ChatGPT Visualizations, UI patterns, prompt engineering, QA, and practical use cases. By Rachmat Efendi.`
- Homepage: `https://rachmatefendi.com`
- Topics: `chatgpt`, `visualizations`, `prompt-engineering`, `data-visualization`, `interactive-tools`, `ui-patterns`, `decision-support`, `playbook`
- Visibility: public
- License: CC BY 4.0 (see [LICENSE](../LICENSE))

A local archive and a Git commit are **not proof of a remote GitHub publication**.
