# Playbook 02 — Build, Test and Review

**Objective:** Make visually convincing results computationally traceable and fit for their stated purpose.

## Test sequence

1. Freeze the input fixture and record a source checksum/period if practical.
2. Independently calculate at least one baseline and one edge-case expected output.
3. Render the requested visual; inspect axis scales, legends, labels and default state.
4. Exercise each control, one at a time; observe all affected charts, KPIs, tables and timelines.
5. Check missing data, zero denominators, negative amounts, date shifts and reset behavior.
6. Test keyboard access, text equivalents, low-contrast labels and color-only information.
7. Check the authority boundary: no factual approval, live status, compliance or guaranteed return claim.
8. Record individual verdicts: **PASS**, **FAIL**, or **NOT TESTED**.
9. If a test fails, simplify or correct the visualization, then rerun only the impacted acceptance suite plus baseline regression.

## Review report format

| Test ID | Source fixture | Expected | Observed | Verdict | Reproduction notes |
|---|---|---|---|---|---|
| CALC-01 | Example | Defined independently | Fill after live run | NOT TESTED | Surface / date / tester |

A documented test plan does not constitute test execution. See [QA documentation](../docs/07-accessibility-and-qa.md).
