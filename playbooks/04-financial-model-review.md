# Playbook 04 — Financial Model Review

**Objective:** Stress-test model calculations and assumptions without making financing, legal or investment decisions.

## Procedure

1. State the decision question and the economic claimant: equity investor, lender, project SPV or issuer.
2. Collect dated inflows/outflows, currencies, fees, taxes, principal movements, document quality and assumptions.
3. Separate historical actuals, self-reported forecasts, independently verified facts and synthetic model inputs.
4. Identify model mechanics: simple/compound interest, effective annual rate, IRR vs XIRR, waterfall and discounting convention.
5. Build a base scenario with a reconciliation table. Reproduce its output independently.
6. Change one stress driver at a time: collection delay, realization haircut, higher costs, refinance constraints or recovery assumptions.
7. Compare cash balance by date, liquidity shortfall, maturity mismatch and concentration risk.
8. Keep uncertainty visible: unknown collateral value is **unknown**, not zero or an implied guarantee.
9. Disclose that no rendered output conveys investment approval, securities advice, formal Sharia/legal opinion or regulatory compliance.

## Test fixture requirements

Provide at least one negative initial outflow and one dated inflow when reporting investor XIRR. If timing is insufficient, report **not calculable** instead of substituting a quoted coupon or target annual return. A stress test should change dates/amounts in a traceable way, not invent collections.

**Indonesia note:** Specify IDR units and calendar/timezone conventions such as `Asia/Jakarta` when material. Local legal, securities or Sukuk questions remain outside the authority of this visualization.
