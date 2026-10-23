# Playbook 01 — Discovery to Visual Prototype

**Objective:** Turn one bounded question into a demonstrable visual without pretending it is production software.

## Standard operating procedure

1. **Frame the decision.** Identify one audience, one question, the smallest acceptable output and what decision the visualization must *not* make.
2. **Identify the source.** Inventory file, table, dataset and authorized connector; record source date, grain, units, classification and access limits.
3. **Choose the visual.** Use the [Decision Guide](../docs/10-decision-guide.md). Start with one visual and at most two meaningful controls.
4. **Specify a data contract.** Declare fields, formulas, keys, scenarios, missing values, rounding and timezone.
5. **Select the surface.** `@Visualize` when supported; if unavailable, request a simpler chart/table or plan a separate application.
6. **Compose prompt.** Use [the base prompt](../templates/prompt-base.md) and define inputs precisely.
7. **Inspect initial output.** Check that controls and underlying values follow the defined contract.
8. **Test baseline and exceptions.** Verify with [the acceptance checklist](../templates/acceptance-checklist.md).
9. **Publish as a prototype.** Show assumptions, data cutoff, non-authoritative status, and next actions.

## Exit criteria

A reproducible prompt, source inventory, declared calculation basis, tested output (or explicit NOT TESTED status), risk note and responsible prototype owner. Do not label the result production-ready.
