# UC-11 — Interactive Technical Education Lab

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** Education / technical concepts  
**Audience:** Teacher, trainer or learner  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

How can changing one physical or mathematical parameter illustrate the underlying mechanism?

## 2. Input and data contract

Named learning objective, governing equation/concept, adjustable parameters with physical bounds, units, reset defaults and clear distinction between demonstration and experimental observation.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Stepwise explanation, interactive parameter probe or slider and optional animation. Include the underlying formula, why the display changes, a knowledge check and accessible textual explanation.

## 4. Copy-ready prompt

```text
@Visualize
Create an interactive explanation of two-source wave interference.
Controls: wavelength, source spacing and phase difference with labeled
units and bounded ranges. Show constructive/destructive interference and
explain each change step by step. Include reset, accessible text, and a
question to check understanding. Treat this as a conceptual model rather
than real measured sensor data.
```

## 5. Acceptance tests

- [ ] Changing wavelength alters the modeled pattern consistently.
- [ ] All parameter units and bounds are visible.
- [ ] Reset restores the stated baseline.
- [ ] Learners can understand the explanation without animation.
- [ ] The result does not claim direct experimental measurement.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

A dynamic picture can be pedagogically useful while still mathematically wrong; validate against a known limiting case and established equations.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
