# UC-07 — Governance & Change-Control Workflow

[← Use Case Index](README.md) · [Evidence](../docs/01-scope-and-evidence.md) · [Acceptance Checklist](../templates/acceptance-checklist.md)

**Domain:** AI governance / software and organizational controls  
**Audience:** Project owner or governance designer  
**Evidence:** Format-level **V**; composite widget arrangements and optional scoring **P**. A similar-looking ChatKit component is not thereby an `@Visualize` public API.

## 1. Decision question

Who may propose, review, authorize, execute and verify a change?

## 2. Input and data contract

Role definitions, allowed transitions, required evidence, draft/approved/implemented/validated state, named approving authority (if formally documented) and transaction boundaries. Missing authority data remains unknown.

**Source policy:** Use only supplied or explicitly authorized sources. Mark fictional training values as synthetic. Do not infer actual results from missing source records.

## 3. Visualization and interaction design

Directed state machine and role-permission matrix. Controls: role and proposed action, with explanation of valid/invalid transition. The UI does not itself validate policy rights or produce an actual decision.

## 4. Copy-ready prompt

```text
@Visualize
Visualize a conceptual change-control process with statuses Proposed,
Reviewed, Approved, Authorized, Executed and Validated, keeping each status
distinct. Display role/action permissions only where supplied by the source.
For unsupported transitions show why they are invalid. Do not infer that a
click, AI response or colorful state badge grants organizational authority.
```

## 5. Acceptance tests

- [ ] Proposed is not Approved or Authorized.
- [ ] Reviewed does not imply executed or validated.
- [ ] An invalid transition visibly fails in the conceptual model.
- [ ] Missing role permission remains unknown.
- [ ] No UI click is described as an actual governance change.


Tests must be executed on a named product surface and dated. Record **PASS / FAIL / NOT TESTED**; a written checklist alone is not evidence of passing tests. Verify keyboard navigation, screen/text fallback, default/reset behavior, and source cutoff.

## 6. Risks and prohibited claims

The visualization cannot enforce identity, approval delegations, document signatures or backend state without a separate authenticated governance runtime.

## 7. Implementation boundary

**Chat visualization:** exploratory what-if analysis or an interactive learning prototype. **Production path:** separately specify identity, authorization, input validation, persistence, audited actions, integration, error handling and monitoring whenever the workflow moves beyond a non-binding visual demonstration.
