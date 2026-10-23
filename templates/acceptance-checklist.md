# Visualization Acceptance Checklist

**Artifact / source:** [ID or filename]  
**Test surface:** [ChatGPT platform/version/account context]  
**Test date / reviewer:** [Date and owner]  
**Result:** PASS / FAIL / NOT TESTED

## Evidence and data

- [ ] Source, period and cutoff are visible.
- [ ] Data grain and deduplication keys are correct.
- [ ] Missing vs zero vs N/A is preserved.
- [ ] Currency, unit and date conventions are explicit.
- [ ] Hypothetical values are not presented as actuals.

## Model and interaction

- [ ] Baseline reconciles to an independently checked fixture.
- [ ] At least one boundary case behaves correctly.
- [ ] Changing a control changes only intended assumptions.
- [ ] Chart, table, KPI and timeline remain synchronized.
- [ ] Reset reproduces baseline; empty state is informative.

## Accessibility and authority

- [ ] Clear labels, visual contrast, readable units and alternative table/text.
- [ ] Keyboard focus, navigation and essential actions work where supported.
- [ ] No live feed, external writeback or approval is falsely implied.
- [ ] Sensitive data is permitted and the share context has been reviewed.

**Do not check a box as PASS unless the case was actually exercised.** Mark unavailable functionality **NOT TESTED** and document the limitation.
