# Accessibility and Quality Assurance

[← Data & State](06-interactivity-and-data.md) · [Security →](08-limitations-security.md)

## Four independent checks

1. **Source fidelity:** source records, row counts, filters, dates, missingness and geographic inputs reconcile.
2. **Numerical correctness:** formulas, scale, units, sign, aggregation and boundary cases are independently checked.
3. **Interaction correctness:** each control changes only intended state; reset, empty state, invalid state and multi-view synchronization work.
4. **Accessible communication:** readable contrast, useful labels, unit labels, keyboard focus, non-color status encoding, text and table fallback.

## Minimal test cases

| Test | Check | Acceptance condition |
|---|---|---|
| Known baseline | Enter an independently calculated fixture | Numeric result and table agree |
| Edge value | Min/max values or missing input | No silent overflow/division by zero |
| Filter isolation | Change selected region | Totals and series change together |
| Scenario isolation | Change only collection delay | Revenue amount stays fixed; dates shift |
| Reset | Return defaults | Baseline is reproduced |
| Accessibility | Keyboard-only navigation | Inputs and result summary remain operable |
| Evidence | Remove a required field | Display N/A/evidence gap, not inferred data |
| Authority | Display illustrative status | No assertion of actual compliance/approval |

## PASS / FAIL reporting

For each case record **test ID, test data version, product surface, observed behavior, expected result, verdict, reproduction notes, test date, and tester**. An unexecuted test is **NOT TESTED**, never PASS. Distinguish editorial checks from actual live product testing.

Use [the acceptance checklist](../templates/acceptance-checklist.md) as the reusable template.
