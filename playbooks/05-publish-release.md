# Playbook 05 — Package, Publish and Maintain

**Objective:** Preserve provenance and ensure release claims match actual verification.

## Release gates

1. Decide license and visibility; **private** is the conservative default while the license is unresolved.
2. Review author attribution, independence disclaimer and rights notice.
3. Confirm all example records and coordinates are synthetic/authorized.
4. Run Markdown link checks, CSV parsing tests and checked numeric fixtures.
5. Verify version, README navigation, directory structure and archive integrity.
6. Record **docs reviewed** and **live product last spot-checked** as separate statuses.
7. On a real GitHub remote, verify initial commit, files, default branch and README rendering.
8. Record release/tag only when actually created and independently confirmed.

## Maintenance and escalation

Monitor official Visualizations docs, ChatKit widget docs and ChatGPT release notes. An impacted section gets **REVIEW REQUIRED** until corroborated. Update only the sections affected by the new evidence; distinguish source change from observed runtime behavior. Full procedure: [Publishing & Maintenance](../docs/11-publishing-and-maintenance.md).
